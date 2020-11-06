---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
ms.openlocfilehash: ad129cfb28aed7670a78550df70d0af410d5dfdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576259"
---
# <span data-ttu-id="20733-101">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="20733-101">New-AzureRmKeyVault</span></span>

## <span data-ttu-id="20733-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20733-102">SYNOPSIS</span></span>
<span data-ttu-id="20733-103">Skapar ett huvud valv.</span><span class="sxs-lookup"><span data-stu-id="20733-103">Creates a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20733-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20733-104">SYNTAX</span></span>

```
New-AzureRmKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete] [-EnablePurgeProtection]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20733-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20733-105">DESCRIPTION</span></span>
<span data-ttu-id="20733-106">Cmdleten **New-AzureRmKeyVault** skapar ett huvud valv i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="20733-106">The **New-AzureRmKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="20733-107">Denna cmdlet beviljar också behörigheter till den inloggade användaren för att lägga till, ta bort eller lista nycklar och hemligheter i nyckel valvet.</span><span class="sxs-lookup"><span data-stu-id="20733-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="20733-108">Obs! Om du får ett fel meddelande om **att prenumerationen inte är registrerad för att använda namn området ' Microsoft. Key valv '** när du försöker skapa ett nytt Key-valv kör du **register-AzureRmResourceProvider-ProviderNamespace "Microsoft. Key Vault"** och kör sedan kommandot **ny-AzureRmKeyVault** .</span><span class="sxs-lookup"><span data-stu-id="20733-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzureRmKeyVault** command.</span></span> <span data-ttu-id="20733-109">Mer information finns i registrera-AzureRmResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="20733-109">For more information, see Register-AzureRmResourceProvider.</span></span>

## <span data-ttu-id="20733-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20733-110">EXAMPLES</span></span>

### <span data-ttu-id="20733-111">Exempel 1: skapa ett standard nyckeltal</span><span class="sxs-lookup"><span data-stu-id="20733-111">Example 1: Create a Standard key vault</span></span>
```powershell
PS C:\> New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'

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

<span data-ttu-id="20733-112">Det här kommandot skapar ett nyckelord med namnet Contoso03Vault i Azure-regionen öst.</span><span class="sxs-lookup"><span data-stu-id="20733-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="20733-113">Kommandot lägger till Key Vault i resurs gruppen med namnet Group14.</span><span class="sxs-lookup"><span data-stu-id="20733-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="20733-114">Eftersom kommandot inte anger ett värde för parametern *SKU* skapar det ett standard-Key-valv.</span><span class="sxs-lookup"><span data-stu-id="20733-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="20733-115">Exempel 2: skapa ett Premium Key-valv</span><span class="sxs-lookup"><span data-stu-id="20733-115">Example 2: Create a Premium key vault</span></span>
```powershell
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'

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

<span data-ttu-id="20733-116">Det här kommandot skapar ett nyckeltal, precis som i föregående exempel.</span><span class="sxs-lookup"><span data-stu-id="20733-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="20733-117">Men det anger ett Premium-värde för parametern *SKU* för att skapa ett Premium Key-valv.</span><span class="sxs-lookup"><span data-stu-id="20733-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="20733-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20733-118">PARAMETERS</span></span>

### <span data-ttu-id="20733-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20733-119">-DefaultProfile</span></span>
<span data-ttu-id="20733-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="20733-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20733-121">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="20733-121">-EnabledForDeployment</span></span>
<span data-ttu-id="20733-122">Gör det möjligt för Microsoft. Compute Resource-leverantören att hämta hemligheter från det här nyckelvärdet när det här nyckelvärdet refereras i resurs skapande, till exempel när du skapar en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="20733-122">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="20733-123">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="20733-123">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="20733-124">Aktiverar tjänsten Azure Disk Encryption för att få hemligheter och unwrap-nycklar från det här nyckel valvet.</span><span class="sxs-lookup"><span data-stu-id="20733-124">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="20733-125">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="20733-125">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="20733-126">Gör det möjligt för Azure Resource Manager att få hemligheter från detta viktiga valv när det här nyckelvärdet refereras till i en mall.</span><span class="sxs-lookup"><span data-stu-id="20733-126">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="20733-127">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="20733-127">-EnablePurgeProtection</span></span>
<span data-ttu-id="20733-128">Om det anges är skyddet mot omedelbar borttagning aktiverat för det här valvet. kräver att mjuka Delete är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="20733-128">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="20733-129">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="20733-129">-EnableSoftDelete</span></span>
<span data-ttu-id="20733-130">Anger att funktionen för mjuka borttagning är aktive rad för det här nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="20733-130">Specifies that the soft-delete functionality is enabled for this key vault.</span></span> <span data-ttu-id="20733-131">När du har aktiverat mjuk borttagning är det möjligt att återställa detta nyckeltal och dess innehåll när det har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="20733-131">When soft-delete is enabled, for a grace period, you can recover this key vault and its contents after it is deleted.</span></span>
<span data-ttu-id="20733-132">Mer information om den här funktionen finns i [Översikt över hur du tar bort Azure Key Vault](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span><span class="sxs-lookup"><span data-stu-id="20733-132">For more information about this functionality, see [Azure Key Vault soft-delete overview](https://docs.microsoft.com/azure/key-vault/key-vault-ovw-soft-delete).</span></span> <span data-ttu-id="20733-133">Instruktioner för hur [du använder nyckelordet Soft – Delete med PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span><span class="sxs-lookup"><span data-stu-id="20733-133">For how-to instructions, see [How to use Key Vault soft-delete with PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-soft-delete-powershell).</span></span>

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

### <span data-ttu-id="20733-134">-Plats</span><span class="sxs-lookup"><span data-stu-id="20733-134">-Location</span></span>
<span data-ttu-id="20733-135">Anger det Azure-område där du vill skapa huvud valvet.</span><span class="sxs-lookup"><span data-stu-id="20733-135">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="20733-136">Använd kommandot [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) för att se dina val.</span><span class="sxs-lookup"><span data-stu-id="20733-136">Use the command [Get-AzureLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzureLocation) to see your choices.</span></span>

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

### <span data-ttu-id="20733-137">-Namn</span><span class="sxs-lookup"><span data-stu-id="20733-137">-Name</span></span>
<span data-ttu-id="20733-138">Anger ett namn på det Key Vault som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="20733-138">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="20733-139">Namnet kan vara en kombination av bokstäver, siffror och bindestreck.</span><span class="sxs-lookup"><span data-stu-id="20733-139">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="20733-140">Namnet måste börja och sluta med en bokstav eller en siffra.</span><span class="sxs-lookup"><span data-stu-id="20733-140">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="20733-141">Namnet måste vara globalt unikt.</span><span class="sxs-lookup"><span data-stu-id="20733-141">The name must be universally unique.</span></span>

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

### <span data-ttu-id="20733-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20733-142">-ResourceGroupName</span></span>
<span data-ttu-id="20733-143">Anger namnet på en befintlig resurs grupp där nyckelords valvet ska skapas.</span><span class="sxs-lookup"><span data-stu-id="20733-143">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="20733-144">-SKU</span><span class="sxs-lookup"><span data-stu-id="20733-144">-Sku</span></span>
<span data-ttu-id="20733-145">Anger SKU för Key valv-instansen.</span><span class="sxs-lookup"><span data-stu-id="20733-145">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="20733-146">Information om vilka funktioner som är tillgängliga för varje SKU finns på webbplatsen för Azure Key Vault prissättning ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="20733-146">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

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

### <span data-ttu-id="20733-147">-Tagg</span><span class="sxs-lookup"><span data-stu-id="20733-147">-Tag</span></span>
<span data-ttu-id="20733-148">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="20733-148">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="20733-149">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="20733-149">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="20733-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="20733-150">-Confirm</span></span>
<span data-ttu-id="20733-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="20733-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20733-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20733-152">-WhatIf</span></span>
<span data-ttu-id="20733-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="20733-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20733-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="20733-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20733-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20733-155">CommonParameters</span></span>
<span data-ttu-id="20733-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20733-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20733-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20733-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20733-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20733-158">INPUTS</span></span>

### <span data-ttu-id="20733-159">System. String</span><span class="sxs-lookup"><span data-stu-id="20733-159">System.String</span></span>

### <span data-ttu-id="20733-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="20733-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="20733-161">Microsoft. Azure. Management. valv. SkuName</span><span class="sxs-lookup"><span data-stu-id="20733-161">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="20733-162">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="20733-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="20733-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20733-163">OUTPUTS</span></span>

### <span data-ttu-id="20733-164">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="20733-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="20733-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20733-165">NOTES</span></span>

## <span data-ttu-id="20733-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20733-166">RELATED LINKS</span></span>

[<span data-ttu-id="20733-167">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="20733-167">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="20733-168">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="20733-168">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
