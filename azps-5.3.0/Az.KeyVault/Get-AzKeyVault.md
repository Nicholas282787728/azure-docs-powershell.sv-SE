---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
ms.openlocfilehash: 37ed0c0cb29e69aa2e8018bb193fa4c82b0c3bcb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520420"
---
# <span data-ttu-id="97380-101">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="97380-101">Get-AzKeyVault</span></span>

## <span data-ttu-id="97380-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="97380-102">SYNOPSIS</span></span>
<span data-ttu-id="97380-103">Hämtar viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="97380-103">Gets key vaults.</span></span>

## <span data-ttu-id="97380-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="97380-104">SYNTAX</span></span>

### <span data-ttu-id="97380-105">GetVaultByName (standard)</span><span class="sxs-lookup"><span data-stu-id="97380-105">GetVaultByName (Default)</span></span>
```
Get-AzKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97380-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="97380-106">ByDeletedVault</span></span>
```
Get-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97380-107">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="97380-107">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97380-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="97380-108">DESCRIPTION</span></span>
<span data-ttu-id="97380-109">Cmdleten **Get-AzKeyVault** hämtar information om viktiga valv i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="97380-109">The **Get-AzKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="97380-110">Du kan visa alla viktiga valv instanser i ett abonnemang eller filtrera dina resultat efter en resurs grupp eller ett visst huvud valv.</span><span class="sxs-lookup"><span data-stu-id="97380-110">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>
<span data-ttu-id="97380-111">Observera att även om du anger resurs gruppen som valfri för denna cmdlet när du får ett enda Key-valv bör du göra det för bättre prestanda.</span><span class="sxs-lookup"><span data-stu-id="97380-111">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="97380-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="97380-112">EXAMPLES</span></span>

### <span data-ttu-id="97380-113">Exempel 1: Hämta alla viktiga valv i ditt nuvarande abonnemang</span><span class="sxs-lookup"><span data-stu-id="97380-113">Example 1: Get all key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVault

Vault Name          : myvault1
Resource Group Name : myrg
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.Ke
                      yVault/vaults/myvault1
Tags                :


Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="97380-114">Det här kommandot får alla viktiga valv i ditt nuvarande abonnemang.</span><span class="sxs-lookup"><span data-stu-id="97380-114">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="97380-115">Exempel 2: skaffa ett speciellt nyckeltal</span><span class="sxs-lookup"><span data-stu-id="97380-115">Example 2: Get a specific key vault</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault'

Vault Name                       : myvault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/myvault
Vault URI                        : https://myvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : True
Enabled For Disk Encryption?     : False
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
```

<span data-ttu-id="97380-116">Det här kommandot får Key-valvet som heter mina valv i ditt nuvarande abonnemang.</span><span class="sxs-lookup"><span data-stu-id="97380-116">This command gets the key vault named myvault in your current subscription.</span></span>

### <span data-ttu-id="97380-117">Exempel 3: Hämta viktiga valv i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="97380-117">Example 3: Get key vaults in a resource group</span></span>
```powershell
PS C:\> Get-AzKeyVault -ResourceGroupName 'myrg1'

Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="97380-118">Det här kommandot får alla viktiga valv i resurs gruppen ContosoPayRollResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="97380-118">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="97380-119">Exempel 4: Hämta alla borttagna nyckeltal till ditt nuvarande abonnemang</span><span class="sxs-lookup"><span data-stu-id="97380-119">Example 4: Get all deleted key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVault -InRemovedState

Vault Name           : myvault4
Location             : westus
Id                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/providers/Microsoft.KeyVault/locations/westu
                       s/deletedVaults/myvault4
Resource ID          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.K
                       eyVault/vaults/myvault4
Deletion Date        : 5/24/2018 9:33:24 PM
Scheduled Purge Date : 8/22/2018 9:33:24 PM
Tags                 :
```

<span data-ttu-id="97380-120">Det här kommandot får alla borttagna Key-valv i ditt nuvarande abonnemang.</span><span class="sxs-lookup"><span data-stu-id="97380-120">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="97380-121">Exempel 5: skaffa ett borttaget nyckeltal</span><span class="sxs-lookup"><span data-stu-id="97380-121">Example 5: Get a deleted key vault</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault4'  -Location 'westus' -InRemovedState

Vault Name           : myvault4
Location             : westus
Id                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/providers/Microsoft.KeyVault/locations/westu
                       s/deletedVaults/myvault4
Resource ID          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.K
                       eyVault/vaults/myvault4
Deletion Date        : 5/24/2018 9:33:24 PM
Scheduled Purge Date : 8/22/2018 9:33:24 PM
Tags                 :
```

<span data-ttu-id="97380-122">Det här kommandot hämtar informationen om viktiga valv som heter myvault4 i ditt nuvarande abonnemang och i regionen Väst.</span><span class="sxs-lookup"><span data-stu-id="97380-122">This command gets the deleted key vault information named myvault4 in your current subscription and in westus region.</span></span>

### <span data-ttu-id="97380-123">Exempel 6: Hämta viktiga valv med hjälp av filtrering</span><span class="sxs-lookup"><span data-stu-id="97380-123">Example 6: Get key vaults using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault*'

Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="97380-124">Det här kommandot får alla viktiga valv i prenumerationen som börjar med "valv".</span><span class="sxs-lookup"><span data-stu-id="97380-124">This command gets all the key vaults in the subscription that start with "myvault".</span></span>

## <span data-ttu-id="97380-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="97380-125">PARAMETERS</span></span>

### <span data-ttu-id="97380-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97380-126">-DefaultProfile</span></span>
<span data-ttu-id="97380-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="97380-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97380-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="97380-128">-InRemovedState</span></span>
<span data-ttu-id="97380-129">Anger om de tidigare borttagna valverna ska visas i resultatet.</span><span class="sxs-lookup"><span data-stu-id="97380-129">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97380-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="97380-130">-Location</span></span>
<span data-ttu-id="97380-131">Platsen för det borttagna valvet.</span><span class="sxs-lookup"><span data-stu-id="97380-131">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97380-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97380-132">-ResourceGroupName</span></span>
<span data-ttu-id="97380-133">Anger namnet på den resurs grupp som är kopplad till Key Vault eller Key vaultes.</span><span class="sxs-lookup"><span data-stu-id="97380-133">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="97380-134">-Tagg</span><span class="sxs-lookup"><span data-stu-id="97380-134">-Tag</span></span>
<span data-ttu-id="97380-135">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="97380-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="97380-136">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="97380-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97380-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="97380-137">-VaultName</span></span>
<span data-ttu-id="97380-138">Anger namnet på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="97380-138">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="97380-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97380-139">CommonParameters</span></span>
<span data-ttu-id="97380-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97380-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97380-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97380-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97380-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="97380-142">INPUTS</span></span>

### <span data-ttu-id="97380-143">System. String</span><span class="sxs-lookup"><span data-stu-id="97380-143">System.String</span></span>

### <span data-ttu-id="97380-144">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="97380-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="97380-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="97380-145">OUTPUTS</span></span>

### <span data-ttu-id="97380-146">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="97380-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="97380-147">Microsoft. Azure. commands. valv. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="97380-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="97380-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="97380-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="97380-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="97380-149">NOTES</span></span>

## <span data-ttu-id="97380-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="97380-150">RELATED LINKS</span></span>

[<span data-ttu-id="97380-151">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="97380-151">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="97380-152">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="97380-152">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
