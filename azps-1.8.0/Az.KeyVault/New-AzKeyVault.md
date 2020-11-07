---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 08f3b7ebaa7b1bc07bdac10b5b7cc16cb4405534
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916310"
---
# <span data-ttu-id="7ef2a-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="7ef2a-101">New-AzKeyVault</span></span>

## <span data-ttu-id="7ef2a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ef2a-102">SYNOPSIS</span></span>
<span data-ttu-id="7ef2a-103">Skapar ett huvud valv.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-103">Creates a key vault.</span></span>

## <span data-ttu-id="7ef2a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ef2a-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete] [-EnablePurgeProtection]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ef2a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ef2a-105">DESCRIPTION</span></span>
<span data-ttu-id="7ef2a-106">Cmdleten **New-AzKeyVault** skapar ett huvud valv i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="7ef2a-107">Denna cmdlet beviljar också behörigheter till den inloggade användaren för att lägga till, ta bort eller lista nycklar och hemligheter i nyckel valvet.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="7ef2a-108">Obs! Om du får ett fel meddelande om **att prenumerationen inte är registrerad för att använda namn området ' Microsoft. Key valv '** när du försöker skapa ett nytt Key-valv kör du **register-AzResourceProvider-ProviderNamespace "Microsoft. Key Vault"** och kör sedan kommandot **ny-AzKeyVault** .</span><span class="sxs-lookup"><span data-stu-id="7ef2a-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="7ef2a-109">Mer information finns i registrera-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="7ef2a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ef2a-110">EXAMPLES</span></span>

### <span data-ttu-id="7ef2a-111">Exempel 1: skapa ett standard nyckeltal</span><span class="sxs-lookup"><span data-stu-id="7ef2a-111">Example 1: Create a Standard key vault</span></span>
```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
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
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore

Tags                             :
```

<span data-ttu-id="7ef2a-112">Det här kommandot skapar ett nyckelord med namnet Contoso03Vault i Azure-regionen öst.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="7ef2a-113">Kommandot lägger till Key Vault i resurs gruppen med namnet Group14.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="7ef2a-114">Eftersom kommandot inte anger ett värde för parametern *SKU* skapar det ett standard-Key-valv.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="7ef2a-115">Exempel 2: skapa ett Premium Key-valv</span><span class="sxs-lookup"><span data-stu-id="7ef2a-115">Example 2: Create a Premium key vault</span></span>
```powershell
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Premium
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
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
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore

Tags                             :
```

<span data-ttu-id="7ef2a-116">Det här kommandot skapar ett nyckeltal, precis som i föregående exempel.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="7ef2a-117">Men det anger ett Premium-värde för parametern *SKU* för att skapa ett Premium Key-valv.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="7ef2a-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ef2a-118">PARAMETERS</span></span>

### <span data-ttu-id="7ef2a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ef2a-119">-DefaultProfile</span></span>
<span data-ttu-id="7ef2a-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7ef2a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ef2a-121">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="7ef2a-121">-EnabledForDeployment</span></span>
<span data-ttu-id="7ef2a-122">Gör det möjligt för Microsoft. Compute Resource-leverantören att hämta hemligheter från det här nyckelvärdet när det här nyckelvärdet refereras i resurs skapande, till exempel när du skapar en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-122">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ef2a-123">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="7ef2a-123">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="7ef2a-124">Aktiverar tjänsten Azure Disk Encryption för att få hemligheter och unwrap-nycklar från det här nyckel valvet.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-124">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ef2a-125">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="7ef2a-125">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="7ef2a-126">Gör det möjligt för Azure Resource Manager att få hemligheter från detta viktiga valv när det här nyckelvärdet refereras till i en mall.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-126">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ef2a-127">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="7ef2a-127">-EnablePurgeProtection</span></span>
<span data-ttu-id="7ef2a-128">Om det anges är skyddet mot omedelbar borttagning aktiverat för det här valvet. kräver att mjuka Delete är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-128">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="7ef2a-129">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="7ef2a-129">-EnableSoftDelete</span></span>
<span data-ttu-id="7ef2a-130">Anger att funktionen för mjuka borttagning är aktive rad för det här nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-130">Specifies that the soft-delete functionality is enabled for this key vault.</span></span> <span data-ttu-id="7ef2a-131">När du har aktiverat mjuk borttagning är det möjligt att återställa detta nyckeltal och dess innehåll när det har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-131">When soft-delete is enabled, for a grace period, you can recover this key vault and its contents after it is deleted.</span></span>
<span data-ttu-id="7ef2a-132">Mer information om den här funktionen finns i [Översikt över hur du tar bort Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span><span class="sxs-lookup"><span data-stu-id="7ef2a-132">For more information about this functionality, see [Azure Key Vault soft-delete overview](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span></span> <span data-ttu-id="7ef2a-133">Instruktioner för hur [du använder nyckelordet Soft – Delete med PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span><span class="sxs-lookup"><span data-stu-id="7ef2a-133">For how-to instructions, see [How to use Key Vault soft-delete with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span></span>

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

### <span data-ttu-id="7ef2a-134">-Plats</span><span class="sxs-lookup"><span data-stu-id="7ef2a-134">-Location</span></span>
<span data-ttu-id="7ef2a-135">Anger det Azure-område där du vill skapa huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-135">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="7ef2a-136">Använd kommandot [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) för att se dina val.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-136">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ef2a-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="7ef2a-137">-Name</span></span>
<span data-ttu-id="7ef2a-138">Anger ett namn på det Key Vault som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-138">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="7ef2a-139">Namnet kan vara en kombination av bokstäver, siffror och bindestreck.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-139">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="7ef2a-140">Namnet måste börja och sluta med en bokstav eller en siffra.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-140">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="7ef2a-141">Namnet måste vara globalt unikt.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-141">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VaultName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ef2a-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ef2a-142">-ResourceGroupName</span></span>
<span data-ttu-id="7ef2a-143">Anger namnet på en befintlig resurs grupp där nyckelords valvet ska skapas.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-143">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ef2a-144">-SKU</span><span class="sxs-lookup"><span data-stu-id="7ef2a-144">-Sku</span></span>
<span data-ttu-id="7ef2a-145">Anger SKU för Key valv-instansen.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-145">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="7ef2a-146">Information om vilka funktioner som är tillgängliga för varje SKU finns på webbplatsen för Azure Key Vault prissättning ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="7ef2a-146">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: Microsoft.Azure.Management.KeyVault.Models.SkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ef2a-147">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7ef2a-147">-Tag</span></span>
<span data-ttu-id="7ef2a-148">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7ef2a-149">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="7ef2a-149">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ef2a-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7ef2a-150">-Confirm</span></span>
<span data-ttu-id="7ef2a-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ef2a-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ef2a-152">-WhatIf</span></span>
<span data-ttu-id="7ef2a-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ef2a-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ef2a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ef2a-155">CommonParameters</span></span>
<span data-ttu-id="7ef2a-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ef2a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ef2a-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ef2a-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ef2a-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ef2a-158">INPUTS</span></span>

### <span data-ttu-id="7ef2a-159">System. String</span><span class="sxs-lookup"><span data-stu-id="7ef2a-159">System.String</span></span>

### <span data-ttu-id="7ef2a-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7ef2a-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="7ef2a-161">Microsoft. Azure. Management. valv. SkuName</span><span class="sxs-lookup"><span data-stu-id="7ef2a-161">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="7ef2a-162">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="7ef2a-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7ef2a-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ef2a-163">OUTPUTS</span></span>

### <span data-ttu-id="7ef2a-164">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="7ef2a-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="7ef2a-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ef2a-165">NOTES</span></span>

## <span data-ttu-id="7ef2a-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ef2a-166">RELATED LINKS</span></span>

[<span data-ttu-id="7ef2a-167">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="7ef2a-167">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="7ef2a-168">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="7ef2a-168">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
