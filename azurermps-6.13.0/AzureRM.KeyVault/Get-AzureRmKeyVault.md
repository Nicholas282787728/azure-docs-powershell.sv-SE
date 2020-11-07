---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: d79c28b09c9f6ca36ae163566574555bb3c50459
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757074"
---
# <span data-ttu-id="9f7be-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="9f7be-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="9f7be-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9f7be-102">SYNOPSIS</span></span>
<span data-ttu-id="9f7be-103">Hämtar viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="9f7be-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f7be-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9f7be-104">SYNTAX</span></span>

### <span data-ttu-id="9f7be-105">ListAllVaultsInSubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="9f7be-105">ListAllVaultsInSubscription (Default)</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f7be-106">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="9f7be-106">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f7be-107">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="9f7be-107">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f7be-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="9f7be-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f7be-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9f7be-109">DESCRIPTION</span></span>
<span data-ttu-id="9f7be-110">Cmdleten **Get-AzureRmKeyVault** hämtar information om viktiga valv i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="9f7be-110">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="9f7be-111">Du kan visa alla viktiga valv instanser i ett abonnemang eller filtrera dina resultat efter en resurs grupp eller ett visst huvud valv.</span><span class="sxs-lookup"><span data-stu-id="9f7be-111">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>
<span data-ttu-id="9f7be-112">Observera att även om du anger resurs gruppen som valfri för denna cmdlet när du får ett enda Key-valv bör du göra det för bättre prestanda.</span><span class="sxs-lookup"><span data-stu-id="9f7be-112">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="9f7be-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9f7be-113">EXAMPLES</span></span>

### <span data-ttu-id="9f7be-114">Exempel 1: Hämta alla viktiga valv i ditt nuvarande abonnemang</span><span class="sxs-lookup"><span data-stu-id="9f7be-114">Example 1: Get all key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzureRMKeyVault

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

<span data-ttu-id="9f7be-115">Det här kommandot får alla viktiga valv i ditt nuvarande abonnemang.</span><span class="sxs-lookup"><span data-stu-id="9f7be-115">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="9f7be-116">Exempel 2: skaffa ett speciellt nyckeltal</span><span class="sxs-lookup"><span data-stu-id="9f7be-116">Example 2: Get a specific key vault</span></span>
```powershell
PS C:\> Get-AzureRMKeyVault -VaultName 'myvault'

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

<span data-ttu-id="9f7be-117">Det här kommandot får Key-valvet som heter mina valv i ditt nuvarande abonnemang.</span><span class="sxs-lookup"><span data-stu-id="9f7be-117">This command gets the key vault named myvault in your current subscription.</span></span>

### <span data-ttu-id="9f7be-118">Exempel 3: Hämta viktiga valv i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="9f7be-118">Example 3: Get key vaults in a resource group</span></span>
```powershell
PS C:\> Get-AzureRmKeyVault -ResourceGroupName 'myrg1'

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

<span data-ttu-id="9f7be-119">Det här kommandot får alla viktiga valv i resurs gruppen ContosoPayRollResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9f7be-119">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="9f7be-120">Exempel 4: Hämta alla borttagna nyckeltal till ditt nuvarande abonnemang</span><span class="sxs-lookup"><span data-stu-id="9f7be-120">Example 4: Get all deleted key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzureRmKeyVault -InRemovedState

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

<span data-ttu-id="9f7be-121">Det här kommandot får alla borttagna Key-valv i ditt nuvarande abonnemang.</span><span class="sxs-lookup"><span data-stu-id="9f7be-121">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="9f7be-122">Exempel 5: skaffa ett borttaget nyckeltal</span><span class="sxs-lookup"><span data-stu-id="9f7be-122">Example 5: Get a deleted key vault</span></span>
```powershell
PS C:\> Get-AzureRMKeyVault -VaultName 'myvault4'  -Location 'westus' -InRemovedState

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

<span data-ttu-id="9f7be-123">Det här kommandot hämtar informationen om viktiga valv som heter myvault4 i ditt nuvarande abonnemang och i regionen Väst.</span><span class="sxs-lookup"><span data-stu-id="9f7be-123">This command gets the deleted key vault information named myvault4 in your current subscription and in westus region.</span></span>

## <span data-ttu-id="9f7be-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9f7be-124">PARAMETERS</span></span>

### <span data-ttu-id="9f7be-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f7be-125">-DefaultProfile</span></span>
<span data-ttu-id="9f7be-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9f7be-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f7be-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="9f7be-127">-InRemovedState</span></span>
<span data-ttu-id="9f7be-128">Anger om de tidigare borttagna valverna ska visas i resultatet.</span><span class="sxs-lookup"><span data-stu-id="9f7be-128">Specifies whether to show the previously deleted vaults in the output.</span></span>

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

### <span data-ttu-id="9f7be-129">-Plats</span><span class="sxs-lookup"><span data-stu-id="9f7be-129">-Location</span></span>
<span data-ttu-id="9f7be-130">Platsen för det borttagna valvet.</span><span class="sxs-lookup"><span data-stu-id="9f7be-130">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="9f7be-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f7be-131">-ResourceGroupName</span></span>
<span data-ttu-id="9f7be-132">Anger namnet på den resurs grupp som är kopplad till Key Vault eller Key vaultes.</span><span class="sxs-lookup"><span data-stu-id="9f7be-132">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f7be-133">-Tagg</span><span class="sxs-lookup"><span data-stu-id="9f7be-133">-Tag</span></span>
<span data-ttu-id="9f7be-134">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="9f7be-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9f7be-135">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="9f7be-135">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f7be-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9f7be-136">-VaultName</span></span>
<span data-ttu-id="9f7be-137">Anger namnet på Key-valvet.</span><span class="sxs-lookup"><span data-stu-id="9f7be-137">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f7be-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f7be-138">CommonParameters</span></span>
<span data-ttu-id="9f7be-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f7be-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f7be-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f7be-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f7be-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9f7be-141">INPUTS</span></span>

### <span data-ttu-id="9f7be-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9f7be-142">System.String</span></span>

### <span data-ttu-id="9f7be-143">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="9f7be-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9f7be-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9f7be-144">OUTPUTS</span></span>

### <span data-ttu-id="9f7be-145">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="9f7be-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="9f7be-146">Microsoft. Azure. commands. valv. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9f7be-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="9f7be-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="9f7be-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="9f7be-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9f7be-148">NOTES</span></span>

## <span data-ttu-id="9f7be-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9f7be-149">RELATED LINKS</span></span>

[<span data-ttu-id="9f7be-150">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="9f7be-150">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="9f7be-151">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="9f7be-151">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
