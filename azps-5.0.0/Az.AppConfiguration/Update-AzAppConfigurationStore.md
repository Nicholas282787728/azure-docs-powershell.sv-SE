---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/update-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
ms.openlocfilehash: 944241dc7434646272c7149d81b380996e71db8f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269671"
---
# <span data-ttu-id="45a51-101">Update-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="45a51-101">Update-AzAppConfigurationStore</span></span>

## <span data-ttu-id="45a51-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="45a51-102">SYNOPSIS</span></span>
<span data-ttu-id="45a51-103">Uppdaterar en konfigurations butik med angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="45a51-103">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="45a51-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="45a51-104">SYNTAX</span></span>

### <span data-ttu-id="45a51-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="45a51-105">UpdateExpanded (Default)</span></span>
```
Update-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyIdentifier <String>] [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="45a51-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="45a51-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-EncryptionKeyIdentifier <String>]
 [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="45a51-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="45a51-107">DESCRIPTION</span></span>
<span data-ttu-id="45a51-108">Uppdaterar en konfigurations butik med angivna parametrar.</span><span class="sxs-lookup"><span data-stu-id="45a51-108">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="45a51-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="45a51-109">EXAMPLES</span></span>

### <span data-ttu-id="45a51-110">Exempel 1: Aktivera data kryptering av programmet conifguration Store med systemtilldelad hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="45a51-110">Example 1: Enable data encryption of the app conifguration store by system-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $systemAssignedAppStore = New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "SystemAssigned"
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $systemAssignedAppStore.IdentityPrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -EncryptionKeyIdentifier $key.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="45a51-111">Det här kommandot aktiverar data kryptering av en nycklar som lagras i ett Azure-valv med en systemtilldelad hanterad identitet.</span><span class="sxs-lookup"><span data-stu-id="45a51-111">This command enables data encryption by a key stored in Azure Key Vault using a system-assigned managed identity.</span></span>
<span data-ttu-id="45a51-112">Valvet måste ha aktiverat mjukt borttagnings-och rensnings skydd och den hanterade identiteten måste ha följande nycklar: get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="45a51-112">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="45a51-113">Exempel 2: Aktivera data kryptering för appen conifguration Store via en användardefinierad hanterad identitet</span><span class="sxs-lookup"><span data-stu-id="45a51-113">Example 2: Enable data encryption of the app conifguration store by user-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $assignedIdentity.PrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test11 -EncryptionKeyIdentifier $key.Id -KeyVaultIdentityClientId $assignedIdentity.ClientId

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="45a51-114">Det här kommandot aktiverar data kryptering av en nycklar som lagras i ett Azure-valv med en användardefinierad hanterad identitet.</span><span class="sxs-lookup"><span data-stu-id="45a51-114">This command enables data encryption by a key stored in Azure Key Vault using a user-assigned managed identity.</span></span>
<span data-ttu-id="45a51-115">Den användardefinierade identiteten måste ha ställts in med `-UserAssignedIdentity` .</span><span class="sxs-lookup"><span data-stu-id="45a51-115">The user-assigned identity must have been set with `-UserAssignedIdentity`.</span></span>
<span data-ttu-id="45a51-116">Valvet måste ha aktiverat mjukt borttagnings-och rensnings skydd och den hanterade identiteten måste ha följande nycklar: get, wrapKey, unwrapKey.</span><span class="sxs-lookup"><span data-stu-id="45a51-116">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="45a51-117">Exempel 3: inaktivera kryptering av en app conifguration Store.</span><span class="sxs-lookup"><span data-stu-id="45a51-117">Example 3: Disable encryption of an app conifguration store.</span></span>
```powershell
PS C:\> $appConf = Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -EncryptionKeyIdentifier $null

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="45a51-118">Det här kommandot inaktiverar kryptering av ett app conifguration-arkiv.</span><span class="sxs-lookup"><span data-stu-id="45a51-118">This command disables encryption of an app conifguration store.</span></span>

### <span data-ttu-id="45a51-119">Exempel 3: uppdatera SKU och tagg för en app conifguration Store via pipeline.</span><span class="sxs-lookup"><span data-stu-id="45a51-119">Example 3: Update sku and tag of an app conifguration store by pipeline.</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -Sku 'standard' -Tag @{'key'='update'}

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="45a51-120">Det här kommandot uppdaterar SKU och tagg för en app conifguration Store via pipeline.</span><span class="sxs-lookup"><span data-stu-id="45a51-120">This command updates sku and tag of an app conifguration store by pipeline.</span></span>

## <span data-ttu-id="45a51-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="45a51-121">PARAMETERS</span></span>

### <span data-ttu-id="45a51-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45a51-122">-AsJob</span></span>
<span data-ttu-id="45a51-123">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="45a51-123">Run the command as a job</span></span>

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

### <span data-ttu-id="45a51-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45a51-124">-DefaultProfile</span></span>
<span data-ttu-id="45a51-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="45a51-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a51-126">-EncryptionKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="45a51-126">-EncryptionKeyIdentifier</span></span>
<span data-ttu-id="45a51-127">URI för Key Vault-tangenten som används för att kryptera data.</span><span class="sxs-lookup"><span data-stu-id="45a51-127">The URI of the key vault key used to encrypt data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a51-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="45a51-128">-IdentityType</span></span>
<span data-ttu-id="45a51-129">Typ av hanterad identitet som används.</span><span class="sxs-lookup"><span data-stu-id="45a51-129">The type of managed identity used.</span></span>
<span data-ttu-id="45a51-130">Typen "SystemAssignedAndUserAssigned" inkluderar både en implicit skapad identitet och en uppsättning användardefinierade identiteter.</span><span class="sxs-lookup"><span data-stu-id="45a51-130">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="45a51-131">Typen "inget" tar bort alla identiteter.</span><span class="sxs-lookup"><span data-stu-id="45a51-131">The type 'None' will remove any identities.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a51-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45a51-132">-InputObject</span></span>
<span data-ttu-id="45a51-133">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="45a51-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45a51-134">-KeyVaultIdentityClientId</span><span class="sxs-lookup"><span data-stu-id="45a51-134">-KeyVaultIdentityClientId</span></span>
<span data-ttu-id="45a51-135">Klient-ID för identiteten som ska användas för att komma åt Key Vault.</span><span class="sxs-lookup"><span data-stu-id="45a51-135">The client id of the identity which will be used to access key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a51-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="45a51-136">-Name</span></span>
<span data-ttu-id="45a51-137">Konfigurations lagrets namn.</span><span class="sxs-lookup"><span data-stu-id="45a51-137">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a51-138">-Nowait</span><span class="sxs-lookup"><span data-stu-id="45a51-138">-NoWait</span></span>
<span data-ttu-id="45a51-139">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="45a51-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="45a51-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45a51-140">-ResourceGroupName</span></span>
<span data-ttu-id="45a51-141">Namnet på resurs gruppen som behållar registret tillhör.</span><span class="sxs-lookup"><span data-stu-id="45a51-141">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a51-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="45a51-142">-Sku</span></span>
<span data-ttu-id="45a51-143">SKU-namnet på konfigurations butiken.</span><span class="sxs-lookup"><span data-stu-id="45a51-143">The SKU name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a51-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="45a51-144">-SubscriptionId</span></span>
<span data-ttu-id="45a51-145">Microsoft Azure-prenumerationens ID.</span><span class="sxs-lookup"><span data-stu-id="45a51-145">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a51-146">-Tagg</span><span class="sxs-lookup"><span data-stu-id="45a51-146">-Tag</span></span>
<span data-ttu-id="45a51-147">Resource-taggarna för ARM.</span><span class="sxs-lookup"><span data-stu-id="45a51-147">The ARM resource tags.</span></span>

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

### <span data-ttu-id="45a51-148">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="45a51-148">-UserAssignedIdentity</span></span>
<span data-ttu-id="45a51-149">Listan över användardefinierade identiteter associerade med resursen.</span><span class="sxs-lookup"><span data-stu-id="45a51-149">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="45a51-150">De användardefinierade nycklarna för identitets ord listor är ARM-resursposter i formatet: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} '.</span><span class="sxs-lookup"><span data-stu-id="45a51-150">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45a51-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="45a51-151">-Confirm</span></span>
<span data-ttu-id="45a51-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="45a51-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45a51-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45a51-153">-WhatIf</span></span>
<span data-ttu-id="45a51-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="45a51-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45a51-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="45a51-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45a51-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45a51-156">CommonParameters</span></span>
<span data-ttu-id="45a51-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45a51-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45a51-158">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45a51-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45a51-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="45a51-159">INPUTS</span></span>

### <span data-ttu-id="45a51-160">Microsoft. Azure. PowerShell. cmdletar. AppConfiguration. Models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="45a51-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="45a51-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="45a51-161">OUTPUTS</span></span>

### <span data-ttu-id="45a51-162">Microsoft. Azure. PowerShell. cmdletar. AppConfiguration. Models. Api20200601. IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="45a51-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="45a51-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="45a51-163">NOTES</span></span>

<span data-ttu-id="45a51-164">ALIAS</span><span class="sxs-lookup"><span data-stu-id="45a51-164">ALIASES</span></span>

<span data-ttu-id="45a51-165">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="45a51-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="45a51-166">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="45a51-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="45a51-167">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="45a51-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="45a51-168">INPUTOBJECT <IAppConfigurationIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="45a51-168">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="45a51-169">`[ConfigStoreName <String>]`: Konfigurations lagrets namn.</span><span class="sxs-lookup"><span data-stu-id="45a51-169">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="45a51-170">`[GroupName <String>]`: Namnet på den privata länk resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="45a51-170">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="45a51-171">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="45a51-171">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="45a51-172">`[PrivateEndpointConnectionName <String>]`: Namn på privat slut punkt</span><span class="sxs-lookup"><span data-stu-id="45a51-172">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="45a51-173">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som behållar registret tillhör.</span><span class="sxs-lookup"><span data-stu-id="45a51-173">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="45a51-174">`[SubscriptionId <String>]`: ID för Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="45a51-174">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="45a51-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="45a51-175">RELATED LINKS</span></span>



<span data-ttu-id="45a51-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0) 
 [New-AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span><span class="sxs-lookup"><span data-stu-id="45a51-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0)
[New-AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span></span>

