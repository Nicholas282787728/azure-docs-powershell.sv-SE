---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: 7cc359b230bc3e4480b1cc6a03db768c17ebf60c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425795"
---
# <span data-ttu-id="1713e-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="1713e-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="1713e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1713e-102">SYNOPSIS</span></span>
<span data-ttu-id="1713e-103">Uppdatera ett Kusto-kluster.</span><span class="sxs-lookup"><span data-stu-id="1713e-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="1713e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1713e-104">SYNTAX</span></span>

### <span data-ttu-id="1713e-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="1713e-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EnableDiskEncryption] [-EnableDoubleEncryption] [-EnablePurge] [-EnableStreamingIngest]
 [-EngineType <EngineType>] [-IdentityType <IdentityType>] [-IdentityUserAssignedIdentity <Hashtable>]
 [-KeyVaultPropertyKeyName <String>] [-KeyVaultPropertyKeyVaultUri <String>]
 [-KeyVaultPropertyKeyVersion <String>] [-KeyVaultPropertyUserIdentity <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1713e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1713e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoCluster -InputObject <IKustoIdentity> [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-EngineType <EngineType>] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-KeyVaultPropertyUserIdentity <String>] [-LanguageExtensionValue <ILanguageExtension[]>]
 [-Location <String>] [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>]
 [-OptimizedAutoscaleMinimum <Int32>] [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>]
 [-SkuName <AzureSkuName>] [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1713e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1713e-107">DESCRIPTION</span></span>
<span data-ttu-id="1713e-108">Uppdatera ett Kusto-kluster.</span><span class="sxs-lookup"><span data-stu-id="1713e-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="1713e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1713e-109">EXAMPLES</span></span>

### <span data-ttu-id="1713e-110">Exempel 1: uppdatera ett befintligt kluster med namn</span><span class="sxs-lookup"><span data-stu-id="1713e-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="1713e-111">Kommandot ovan uppdaterar SKU för Kusto-klustret "testnewkustocluster" i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="1713e-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="1713e-112">Exempel 2: uppdatera ett befintligt kluster med namn</span><span class="sxs-lookup"><span data-stu-id="1713e-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="1713e-113">Kommandot ovan uppdaterar klustret "testnewkustocluster" i resurs gruppen "testrg" med en hanterad kund.</span><span class="sxs-lookup"><span data-stu-id="1713e-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="1713e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1713e-114">PARAMETERS</span></span>

### <span data-ttu-id="1713e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1713e-115">-AsJob</span></span>
<span data-ttu-id="1713e-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="1713e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="1713e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1713e-117">-DefaultProfile</span></span>
<span data-ttu-id="1713e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1713e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1713e-119">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="1713e-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="1713e-120">Ett booleskt värde som anger om klustrets diskar är krypterade.</span><span class="sxs-lookup"><span data-stu-id="1713e-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="1713e-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="1713e-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="1713e-122">Ett booleskt värde som anger om Double Encryption är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="1713e-122">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="1713e-123">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="1713e-123">-EnablePurge</span></span>
<span data-ttu-id="1713e-124">Ett booleskt värde som anger om rensningen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="1713e-124">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="1713e-125">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="1713e-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="1713e-126">Ett booleskt värde som anger om streaming-funktionen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="1713e-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="1713e-127">-EngineType</span><span class="sxs-lookup"><span data-stu-id="1713e-127">-EngineType</span></span>
<span data-ttu-id="1713e-128">Motor typen</span><span class="sxs-lookup"><span data-stu-id="1713e-128">The engine type</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.EngineType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1713e-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="1713e-129">-IdentityType</span></span>
<span data-ttu-id="1713e-130">Typ av hanterad identitet som används.</span><span class="sxs-lookup"><span data-stu-id="1713e-130">The type of managed identity used.</span></span>
<span data-ttu-id="1713e-131">Typen ' SystemAssigned, UserAssigned ' inkluderar både en implicit skapad identitet och en uppsättning användardefinierade identiteter.</span><span class="sxs-lookup"><span data-stu-id="1713e-131">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="1713e-132">Typen "inget" tar bort alla identiteter.</span><span class="sxs-lookup"><span data-stu-id="1713e-132">The type 'None' will remove all identities.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1713e-133">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="1713e-133">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="1713e-134">Listan över användar identiteter som är kopplade till Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="1713e-134">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="1713e-135">Nyckelorden för användar identitets ord lista är ARM resurs-ID i formatet: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} '.</span><span class="sxs-lookup"><span data-stu-id="1713e-135">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="1713e-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1713e-136">-InputObject</span></span>
<span data-ttu-id="1713e-137">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="1713e-137">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1713e-138">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="1713e-138">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="1713e-139">Namnet på Key valv-tangenten.</span><span class="sxs-lookup"><span data-stu-id="1713e-139">The name of the key vault key.</span></span>

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

### <span data-ttu-id="1713e-140">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="1713e-140">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="1713e-141">URI för Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1713e-141">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="1713e-142">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="1713e-142">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="1713e-143">Versionen av Key valv-tangenten.</span><span class="sxs-lookup"><span data-stu-id="1713e-143">The version of the key vault key.</span></span>

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

### <span data-ttu-id="1713e-144">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="1713e-144">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="1713e-145">Den användare tilldelade identiteten (ARM Resource-ID) som har åtkomst till den.</span><span class="sxs-lookup"><span data-stu-id="1713e-145">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="1713e-146">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="1713e-146">-LanguageExtensionValue</span></span>
<span data-ttu-id="1713e-147">Listan över språk tillägg.</span><span class="sxs-lookup"><span data-stu-id="1713e-147">The list of language extensions.</span></span>
<span data-ttu-id="1713e-148">För att konstruera kan du läsa avsnittet anteckningar för LANGUAGEEXTENSIONVALUE-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="1713e-148">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1713e-149">-Plats</span><span class="sxs-lookup"><span data-stu-id="1713e-149">-Location</span></span>
<span data-ttu-id="1713e-150">Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="1713e-150">Resource location.</span></span>

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

### <span data-ttu-id="1713e-151">-Namn</span><span class="sxs-lookup"><span data-stu-id="1713e-151">-Name</span></span>
<span data-ttu-id="1713e-152">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="1713e-152">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1713e-153">-Nowait</span><span class="sxs-lookup"><span data-stu-id="1713e-153">-NoWait</span></span>
<span data-ttu-id="1713e-154">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="1713e-154">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1713e-155">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="1713e-155">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="1713e-156">Ett booleskt värde som anger om den optimerade autoskalningsfunktionen är aktive rad eller inte.</span><span class="sxs-lookup"><span data-stu-id="1713e-156">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="1713e-157">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="1713e-157">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="1713e-158">Maximalt antal tillåtna instanser.</span><span class="sxs-lookup"><span data-stu-id="1713e-158">Maximum allowed instances count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1713e-159">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="1713e-159">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="1713e-160">Antal tillåtna instanser.</span><span class="sxs-lookup"><span data-stu-id="1713e-160">Minimum allowed instances count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1713e-161">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="1713e-161">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="1713e-162">Versionen av den definierade mallen, till exempel 1.</span><span class="sxs-lookup"><span data-stu-id="1713e-162">The version of the template defined, for instance 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1713e-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1713e-163">-ResourceGroupName</span></span>
<span data-ttu-id="1713e-164">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="1713e-164">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="1713e-165">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="1713e-165">-SkuCapacity</span></span>
<span data-ttu-id="1713e-166">Antalet instanser av klustret.</span><span class="sxs-lookup"><span data-stu-id="1713e-166">The number of instances of the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1713e-167">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1713e-167">-SkuName</span></span>
<span data-ttu-id="1713e-168">SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="1713e-168">SKU name.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1713e-169">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="1713e-169">-SkuTier</span></span>
<span data-ttu-id="1713e-170">SKU-nivå.</span><span class="sxs-lookup"><span data-stu-id="1713e-170">SKU tier.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuTier
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1713e-171">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1713e-171">-SubscriptionId</span></span>
<span data-ttu-id="1713e-172">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="1713e-172">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1713e-173">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="1713e-173">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1713e-174">-Tagg</span><span class="sxs-lookup"><span data-stu-id="1713e-174">-Tag</span></span>
<span data-ttu-id="1713e-175">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="1713e-175">Resource tags.</span></span>

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

### <span data-ttu-id="1713e-176">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="1713e-176">-TrustedExternalTenant</span></span>
<span data-ttu-id="1713e-177">Klustrets externa klient organisationer.</span><span class="sxs-lookup"><span data-stu-id="1713e-177">The cluster's external tenants.</span></span>
<span data-ttu-id="1713e-178">För att konstruera kan du läsa avsnittet anteckningar för TRUSTEDEXTERNALTENANT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="1713e-178">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ITrustedExternalTenant[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1713e-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="1713e-179">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="1713e-180">Resurs-ID för offentlig IP-adress för data hantering.</span><span class="sxs-lookup"><span data-stu-id="1713e-180">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="1713e-181">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="1713e-181">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="1713e-182">Motor tjänstens resurs-ID för offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="1713e-182">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="1713e-183">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="1713e-183">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="1713e-184">ID för under nätets resurs.</span><span class="sxs-lookup"><span data-stu-id="1713e-184">The subnet resource id.</span></span>

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

### <span data-ttu-id="1713e-185">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1713e-185">-Confirm</span></span>
<span data-ttu-id="1713e-186">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1713e-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1713e-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1713e-187">-WhatIf</span></span>
<span data-ttu-id="1713e-188">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1713e-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1713e-189">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1713e-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1713e-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1713e-190">CommonParameters</span></span>
<span data-ttu-id="1713e-191">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1713e-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1713e-192">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1713e-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1713e-193">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1713e-193">INPUTS</span></span>

### <span data-ttu-id="1713e-194">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="1713e-194">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="1713e-195">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1713e-195">OUTPUTS</span></span>

### <span data-ttu-id="1713e-196">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200918. ICluster</span><span class="sxs-lookup"><span data-stu-id="1713e-196">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="1713e-197">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1713e-197">NOTES</span></span>

<span data-ttu-id="1713e-198">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1713e-198">ALIASES</span></span>

<span data-ttu-id="1713e-199">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="1713e-199">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1713e-200">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="1713e-200">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1713e-201">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1713e-201">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1713e-202">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="1713e-202">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1713e-203">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="1713e-203">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="1713e-204">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="1713e-204">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="1713e-205">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="1713e-205">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="1713e-206">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="1713e-206">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="1713e-207">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="1713e-207">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1713e-208">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="1713e-208">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="1713e-209">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="1713e-209">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="1713e-210">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="1713e-210">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="1713e-211">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="1713e-211">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1713e-212">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="1713e-212">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="1713e-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >: listan med språk tillägg.</span><span class="sxs-lookup"><span data-stu-id="1713e-213">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="1713e-214">`[Name <LanguageExtensionName?>]`: Namnet på språk tillägget.</span><span class="sxs-lookup"><span data-stu-id="1713e-214">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="1713e-215">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: klustrets externa klient organisationer.</span><span class="sxs-lookup"><span data-stu-id="1713e-215">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="1713e-216">`[Value <String>]`: GUID som representerar en extern klient organisation.</span><span class="sxs-lookup"><span data-stu-id="1713e-216">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="1713e-217">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1713e-217">RELATED LINKS</span></span>

