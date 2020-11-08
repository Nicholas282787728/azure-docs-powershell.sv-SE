---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: a3e1561feb470708420015bac1e2f0688f182896
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270948"
---
# <span data-ttu-id="eed3d-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="eed3d-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="eed3d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eed3d-102">SYNOPSIS</span></span>
<span data-ttu-id="eed3d-103">Uppdatera ett Kusto-kluster.</span><span class="sxs-lookup"><span data-stu-id="eed3d-103">Update a Kusto cluster.</span></span>

## <span data-ttu-id="eed3d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eed3d-104">SYNTAX</span></span>

### <span data-ttu-id="eed3d-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="eed3d-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EnableDiskEncryption] [-EnableDoubleEncryption] [-EnablePurge] [-EnableStreamingIngest]
 [-IdentityType <IdentityType>] [-IdentityUserAssignedIdentity <Hashtable>]
 [-KeyVaultPropertyKeyName <String>] [-KeyVaultPropertyKeyVaultUri <String>]
 [-KeyVaultPropertyKeyVersion <String>] [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>]
 [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="eed3d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="eed3d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoCluster -InputObject <IKustoIdentity> [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-Location <String>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-SkuName <AzureSkuName>]
 [-SkuTier <AzureSkuTier>] [-Tag <Hashtable>] [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="eed3d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eed3d-107">DESCRIPTION</span></span>
<span data-ttu-id="eed3d-108">Uppdatera ett Kusto-kluster.</span><span class="sxs-lookup"><span data-stu-id="eed3d-108">Update a Kusto cluster.</span></span>

## <span data-ttu-id="eed3d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eed3d-109">EXAMPLES</span></span>

### <span data-ttu-id="eed3d-110">Exempel 1: uppdatera ett befintligt kluster med namn</span><span class="sxs-lookup"><span data-stu-id="eed3d-110">Example 1: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -SkuName Standard_D12_v2 -SkuTier Standard

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="eed3d-111">Kommandot ovan uppdaterar SKU för Kusto-klustret "testnewkustocluster" i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="eed3d-111">The above command updates the sku of the Kusto cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="eed3d-112">Exempel 2: uppdatera ett befintligt kluster med namn</span><span class="sxs-lookup"><span data-stu-id="eed3d-112">Example 2: Update an existing cluster by name</span></span>
```powershell
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -KeyVaultPropertyKeyName "TestKey" -KeyVaultPropertyKeyVaultUri "https://testpskeyvault.vault.azure.net" -KeyVaultPropertyKeyVersion "4bd66f0e0d7c403fac80305e0355d982"

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="eed3d-113">Kommandot ovan uppdaterar klustret "testnewkustocluster" i resurs gruppen "testrg" med en hanterad kund.</span><span class="sxs-lookup"><span data-stu-id="eed3d-113">The above command updates the cluster "testnewkustocluster" found in the resource group "testrg" with a customer managed key.</span></span>

## <span data-ttu-id="eed3d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eed3d-114">PARAMETERS</span></span>

### <span data-ttu-id="eed3d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eed3d-115">-AsJob</span></span>
<span data-ttu-id="eed3d-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="eed3d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="eed3d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eed3d-117">-DefaultProfile</span></span>
<span data-ttu-id="eed3d-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eed3d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eed3d-119">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="eed3d-119">-EnableDiskEncryption</span></span>
<span data-ttu-id="eed3d-120">Ett booleskt värde som anger om klustrets diskar är krypterade.</span><span class="sxs-lookup"><span data-stu-id="eed3d-120">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="eed3d-121">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="eed3d-121">-EnableDoubleEncryption</span></span>
<span data-ttu-id="eed3d-122">Ett booleskt värde som anger om Double Encryption är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="eed3d-122">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="eed3d-123">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="eed3d-123">-EnablePurge</span></span>
<span data-ttu-id="eed3d-124">Ett booleskt värde som anger om rensningen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="eed3d-124">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="eed3d-125">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="eed3d-125">-EnableStreamingIngest</span></span>
<span data-ttu-id="eed3d-126">Ett booleskt värde som anger om streaming-funktionen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="eed3d-126">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="eed3d-127">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="eed3d-127">-IdentityType</span></span>
<span data-ttu-id="eed3d-128">Identitets typen.</span><span class="sxs-lookup"><span data-stu-id="eed3d-128">The identity type.</span></span>

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

### <span data-ttu-id="eed3d-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="eed3d-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="eed3d-130">Listan över användar identiteter som är kopplade till Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="eed3d-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="eed3d-131">Nyckelorden för användar identitets ord lista är ARM resurs-ID i formatet: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} '.</span><span class="sxs-lookup"><span data-stu-id="eed3d-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="eed3d-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eed3d-132">-InputObject</span></span>
<span data-ttu-id="eed3d-133">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="eed3d-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="eed3d-134">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="eed3d-134">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="eed3d-135">Namnet på Key valv-tangenten.</span><span class="sxs-lookup"><span data-stu-id="eed3d-135">The name of the key vault key.</span></span>

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

### <span data-ttu-id="eed3d-136">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="eed3d-136">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="eed3d-137">URI för Key Vault.</span><span class="sxs-lookup"><span data-stu-id="eed3d-137">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="eed3d-138">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="eed3d-138">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="eed3d-139">Versionen av Key valv-tangenten.</span><span class="sxs-lookup"><span data-stu-id="eed3d-139">The version of the key vault key.</span></span>

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

### <span data-ttu-id="eed3d-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="eed3d-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="eed3d-141">Listan över språk tillägg.</span><span class="sxs-lookup"><span data-stu-id="eed3d-141">The list of language extensions.</span></span>
<span data-ttu-id="eed3d-142">För att konstruera kan du läsa avsnittet anteckningar för LANGUAGEEXTENSIONVALUE-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="eed3d-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eed3d-143">-Plats</span><span class="sxs-lookup"><span data-stu-id="eed3d-143">-Location</span></span>
<span data-ttu-id="eed3d-144">Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="eed3d-144">Resource location.</span></span>

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

### <span data-ttu-id="eed3d-145">-Namn</span><span class="sxs-lookup"><span data-stu-id="eed3d-145">-Name</span></span>
<span data-ttu-id="eed3d-146">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="eed3d-146">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="eed3d-147">-Nowait</span><span class="sxs-lookup"><span data-stu-id="eed3d-147">-NoWait</span></span>
<span data-ttu-id="eed3d-148">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="eed3d-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="eed3d-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="eed3d-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="eed3d-150">Ett booleskt värde som anger om den optimerade autoskalningsfunktionen är aktive rad eller inte.</span><span class="sxs-lookup"><span data-stu-id="eed3d-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="eed3d-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="eed3d-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="eed3d-152">Maximalt antal tillåtna instanser.</span><span class="sxs-lookup"><span data-stu-id="eed3d-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="eed3d-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="eed3d-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="eed3d-154">Antal tillåtna instanser.</span><span class="sxs-lookup"><span data-stu-id="eed3d-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="eed3d-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="eed3d-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="eed3d-156">Versionen av den definierade mallen, till exempel 1.</span><span class="sxs-lookup"><span data-stu-id="eed3d-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="eed3d-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eed3d-157">-ResourceGroupName</span></span>
<span data-ttu-id="eed3d-158">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="eed3d-158">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="eed3d-159">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="eed3d-159">-SkuCapacity</span></span>
<span data-ttu-id="eed3d-160">Antalet instanser av klustret.</span><span class="sxs-lookup"><span data-stu-id="eed3d-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="eed3d-161">-SkuName</span><span class="sxs-lookup"><span data-stu-id="eed3d-161">-SkuName</span></span>
<span data-ttu-id="eed3d-162">SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="eed3d-162">SKU name.</span></span>

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

### <span data-ttu-id="eed3d-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="eed3d-163">-SkuTier</span></span>
<span data-ttu-id="eed3d-164">SKU-nivå.</span><span class="sxs-lookup"><span data-stu-id="eed3d-164">SKU tier.</span></span>

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

### <span data-ttu-id="eed3d-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eed3d-165">-SubscriptionId</span></span>
<span data-ttu-id="eed3d-166">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="eed3d-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="eed3d-167">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="eed3d-167">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="eed3d-168">-Tagg</span><span class="sxs-lookup"><span data-stu-id="eed3d-168">-Tag</span></span>
<span data-ttu-id="eed3d-169">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="eed3d-169">Resource tags.</span></span>

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

### <span data-ttu-id="eed3d-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="eed3d-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="eed3d-171">Klustrets externa klient organisationer.</span><span class="sxs-lookup"><span data-stu-id="eed3d-171">The cluster's external tenants.</span></span>
<span data-ttu-id="eed3d-172">För att konstruera kan du läsa avsnittet anteckningar för TRUSTEDEXTERNALTENANT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="eed3d-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ITrustedExternalTenant[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eed3d-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="eed3d-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="eed3d-174">Resurs-ID för offentlig IP-adress för data hantering.</span><span class="sxs-lookup"><span data-stu-id="eed3d-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="eed3d-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="eed3d-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="eed3d-176">Motor tjänstens resurs-ID för offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="eed3d-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="eed3d-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="eed3d-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="eed3d-178">ID för under nätets resurs.</span><span class="sxs-lookup"><span data-stu-id="eed3d-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="eed3d-179">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eed3d-179">-Confirm</span></span>
<span data-ttu-id="eed3d-180">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eed3d-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eed3d-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eed3d-181">-WhatIf</span></span>
<span data-ttu-id="eed3d-182">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eed3d-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eed3d-183">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eed3d-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eed3d-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eed3d-184">CommonParameters</span></span>
<span data-ttu-id="eed3d-185">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eed3d-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eed3d-186">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eed3d-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eed3d-187">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eed3d-187">INPUTS</span></span>

### <span data-ttu-id="eed3d-188">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="eed3d-188">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="eed3d-189">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eed3d-189">OUTPUTS</span></span>

### <span data-ttu-id="eed3d-190">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. ICluster</span><span class="sxs-lookup"><span data-stu-id="eed3d-190">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="eed3d-191">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eed3d-191">NOTES</span></span>

<span data-ttu-id="eed3d-192">ALIAS</span><span class="sxs-lookup"><span data-stu-id="eed3d-192">ALIASES</span></span>

<span data-ttu-id="eed3d-193">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="eed3d-193">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="eed3d-194">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="eed3d-194">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="eed3d-195">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="eed3d-195">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="eed3d-196">INPUTOBJECT <IKustoIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="eed3d-196">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="eed3d-197">`[AttachedDatabaseConfigurationName <String>]`: Namnet på den anslutna databas konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="eed3d-197">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="eed3d-198">`[ClusterName <String>]`: Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="eed3d-198">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="eed3d-199">`[DataConnectionName <String>]`: Namnet på data anslutningen.</span><span class="sxs-lookup"><span data-stu-id="eed3d-199">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="eed3d-200">`[DatabaseName <String>]`: Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="eed3d-200">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="eed3d-201">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="eed3d-201">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="eed3d-202">`[Location <String>]`: Azure-plats.</span><span class="sxs-lookup"><span data-stu-id="eed3d-202">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="eed3d-203">`[PrincipalAssignmentName <String>]`: Namnet på Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="eed3d-203">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="eed3d-204">`[ResourceGroupName <String>]`: Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="eed3d-204">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="eed3d-205">`[SubscriptionId <String>]`: Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="eed3d-205">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="eed3d-206">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="eed3d-206">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="eed3d-207">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >: listan med språk tillägg.</span><span class="sxs-lookup"><span data-stu-id="eed3d-207">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="eed3d-208">`[Name <LanguageExtensionName?>]`: Namnet på språk tillägget.</span><span class="sxs-lookup"><span data-stu-id="eed3d-208">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="eed3d-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: klustrets externa klient organisationer.</span><span class="sxs-lookup"><span data-stu-id="eed3d-209">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="eed3d-210">`[Value <String>]`: GUID som representerar en extern klient organisation.</span><span class="sxs-lookup"><span data-stu-id="eed3d-210">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="eed3d-211">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eed3d-211">RELATED LINKS</span></span>

