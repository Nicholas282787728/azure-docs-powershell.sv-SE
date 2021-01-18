---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: b868633f0217b2048f0a83641f678e9c092d21c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524096"
---
# <span data-ttu-id="ac405-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="ac405-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="ac405-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ac405-102">SYNOPSIS</span></span>
<span data-ttu-id="ac405-103">Skapa eller uppdatera ett Kusto-kluster.</span><span class="sxs-lookup"><span data-stu-id="ac405-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="ac405-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ac405-104">SYNTAX</span></span>

```
New-AzKustoCluster -Name <String> -ResourceGroupName <String> -Location <String> -SkuName <AzureSkuName>
 -SkuTier <AzureSkuTier> [-SubscriptionId <String>] [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-EngineType <EngineType>] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-KeyVaultPropertyUserIdentity <String>] [-LanguageExtensionValue <ILanguageExtension[]>]
 [-OptimizedAutoscaleIsEnabled] [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ac405-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ac405-105">DESCRIPTION</span></span>
<span data-ttu-id="ac405-106">Skapa eller uppdatera ett Kusto-kluster.</span><span class="sxs-lookup"><span data-stu-id="ac405-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="ac405-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ac405-107">EXAMPLES</span></span>

### <span data-ttu-id="ac405-108">Exempel 1: skapa ett nytt Kusto-kluster</span><span class="sxs-lookup"><span data-stu-id="ac405-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true -EngineType 'V2'

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="ac405-109">Med kommandot ovan skapas ett nytt Kusto-kluster med namnet "testnewkustocluster" i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="ac405-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="ac405-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ac405-110">PARAMETERS</span></span>

### <span data-ttu-id="ac405-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac405-111">-AsJob</span></span>
<span data-ttu-id="ac405-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="ac405-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ac405-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac405-113">-DefaultProfile</span></span>
<span data-ttu-id="ac405-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ac405-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac405-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="ac405-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="ac405-116">Ett booleskt värde som anger om klustrets diskar är krypterade.</span><span class="sxs-lookup"><span data-stu-id="ac405-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="ac405-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="ac405-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="ac405-118">Ett booleskt värde som anger om Double Encryption är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="ac405-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="ac405-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="ac405-119">-EnablePurge</span></span>
<span data-ttu-id="ac405-120">Ett booleskt värde som anger om rensningen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="ac405-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="ac405-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="ac405-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="ac405-122">Ett booleskt värde som anger om streaming-funktionen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="ac405-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="ac405-123">-EngineType</span><span class="sxs-lookup"><span data-stu-id="ac405-123">-EngineType</span></span>
<span data-ttu-id="ac405-124">Motor typen</span><span class="sxs-lookup"><span data-stu-id="ac405-124">The engine type</span></span>

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

### <span data-ttu-id="ac405-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="ac405-125">-IdentityType</span></span>
<span data-ttu-id="ac405-126">Typ av hanterad identitet som används.</span><span class="sxs-lookup"><span data-stu-id="ac405-126">The type of managed identity used.</span></span>
<span data-ttu-id="ac405-127">Typen ' SystemAssigned, UserAssigned ' inkluderar både en implicit skapad identitet och en uppsättning användardefinierade identiteter.</span><span class="sxs-lookup"><span data-stu-id="ac405-127">The type 'SystemAssigned, UserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="ac405-128">Typen "inget" tar bort alla identiteter.</span><span class="sxs-lookup"><span data-stu-id="ac405-128">The type 'None' will remove all identities.</span></span>

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

### <span data-ttu-id="ac405-129">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ac405-129">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="ac405-130">Listan över användar identiteter som är kopplade till Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="ac405-130">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="ac405-131">Nyckelorden för användar identitets ord lista är ARM resurs-ID i formatet: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} '.</span><span class="sxs-lookup"><span data-stu-id="ac405-131">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="ac405-132">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="ac405-132">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="ac405-133">Namnet på Key valv-tangenten.</span><span class="sxs-lookup"><span data-stu-id="ac405-133">The name of the key vault key.</span></span>

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

### <span data-ttu-id="ac405-134">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="ac405-134">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="ac405-135">URI för Key Vault.</span><span class="sxs-lookup"><span data-stu-id="ac405-135">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="ac405-136">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="ac405-136">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="ac405-137">Versionen av Key valv-tangenten.</span><span class="sxs-lookup"><span data-stu-id="ac405-137">The version of the key vault key.</span></span>

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

### <span data-ttu-id="ac405-138">-KeyVaultPropertyUserIdentity</span><span class="sxs-lookup"><span data-stu-id="ac405-138">-KeyVaultPropertyUserIdentity</span></span>
<span data-ttu-id="ac405-139">Den användare tilldelade identiteten (ARM Resource-ID) som har åtkomst till den.</span><span class="sxs-lookup"><span data-stu-id="ac405-139">The user assigned identity (ARM resource id) that has access to the key.</span></span>

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

### <span data-ttu-id="ac405-140">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="ac405-140">-LanguageExtensionValue</span></span>
<span data-ttu-id="ac405-141">Listan över språk tillägg.</span><span class="sxs-lookup"><span data-stu-id="ac405-141">The list of language extensions.</span></span>
<span data-ttu-id="ac405-142">För att konstruera kan du läsa avsnittet anteckningar för LANGUAGEEXTENSIONVALUE-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="ac405-142">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ac405-143">-Plats</span><span class="sxs-lookup"><span data-stu-id="ac405-143">-Location</span></span>
<span data-ttu-id="ac405-144">Den Geo-plats där resursen bor</span><span class="sxs-lookup"><span data-stu-id="ac405-144">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac405-145">-Namn</span><span class="sxs-lookup"><span data-stu-id="ac405-145">-Name</span></span>
<span data-ttu-id="ac405-146">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="ac405-146">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac405-147">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ac405-147">-NoWait</span></span>
<span data-ttu-id="ac405-148">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="ac405-148">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ac405-149">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="ac405-149">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="ac405-150">Ett booleskt värde som anger om den optimerade autoskalningsfunktionen är aktive rad eller inte.</span><span class="sxs-lookup"><span data-stu-id="ac405-150">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="ac405-151">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="ac405-151">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="ac405-152">Maximalt antal tillåtna instanser.</span><span class="sxs-lookup"><span data-stu-id="ac405-152">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="ac405-153">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="ac405-153">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="ac405-154">Antal tillåtna instanser.</span><span class="sxs-lookup"><span data-stu-id="ac405-154">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="ac405-155">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="ac405-155">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="ac405-156">Versionen av den definierade mallen, till exempel 1.</span><span class="sxs-lookup"><span data-stu-id="ac405-156">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="ac405-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac405-157">-ResourceGroupName</span></span>
<span data-ttu-id="ac405-158">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="ac405-158">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac405-159">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ac405-159">-SkuCapacity</span></span>
<span data-ttu-id="ac405-160">Antalet instanser av klustret.</span><span class="sxs-lookup"><span data-stu-id="ac405-160">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="ac405-161">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ac405-161">-SkuName</span></span>
<span data-ttu-id="ac405-162">SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="ac405-162">SKU name.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac405-163">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ac405-163">-SkuTier</span></span>
<span data-ttu-id="ac405-164">SKU-nivå.</span><span class="sxs-lookup"><span data-stu-id="ac405-164">SKU tier.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.AzureSkuTier
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac405-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac405-165">-SubscriptionId</span></span>
<span data-ttu-id="ac405-166">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="ac405-166">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ac405-167">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="ac405-167">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac405-168">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ac405-168">-Tag</span></span>
<span data-ttu-id="ac405-169">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="ac405-169">Resource tags.</span></span>

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

### <span data-ttu-id="ac405-170">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="ac405-170">-TrustedExternalTenant</span></span>
<span data-ttu-id="ac405-171">Klustrets externa klient organisationer.</span><span class="sxs-lookup"><span data-stu-id="ac405-171">The cluster's external tenants.</span></span>
<span data-ttu-id="ac405-172">För att konstruera kan du läsa avsnittet anteckningar för TRUSTEDEXTERNALTENANT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="ac405-172">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ac405-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="ac405-173">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="ac405-174">Resurs-ID för offentlig IP-adress för data hantering.</span><span class="sxs-lookup"><span data-stu-id="ac405-174">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="ac405-175">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="ac405-175">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="ac405-176">Motor tjänstens resurs-ID för offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="ac405-176">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="ac405-177">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="ac405-177">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="ac405-178">ID för under nätets resurs.</span><span class="sxs-lookup"><span data-stu-id="ac405-178">The subnet resource id.</span></span>

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

### <span data-ttu-id="ac405-179">-Zone</span><span class="sxs-lookup"><span data-stu-id="ac405-179">-Zone</span></span>
<span data-ttu-id="ac405-180">Klustrets tillgänglighets zoner.</span><span class="sxs-lookup"><span data-stu-id="ac405-180">The availability zones of the cluster.</span></span>

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

### <span data-ttu-id="ac405-181">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ac405-181">-Confirm</span></span>
<span data-ttu-id="ac405-182">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ac405-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac405-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac405-183">-WhatIf</span></span>
<span data-ttu-id="ac405-184">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ac405-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac405-185">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ac405-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac405-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac405-186">CommonParameters</span></span>
<span data-ttu-id="ac405-187">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac405-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac405-188">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac405-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac405-189">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ac405-189">INPUTS</span></span>

## <span data-ttu-id="ac405-190">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ac405-190">OUTPUTS</span></span>

### <span data-ttu-id="ac405-191">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200918. ICluster</span><span class="sxs-lookup"><span data-stu-id="ac405-191">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="ac405-192">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ac405-192">NOTES</span></span>

<span data-ttu-id="ac405-193">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ac405-193">ALIASES</span></span>

<span data-ttu-id="ac405-194">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="ac405-194">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ac405-195">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="ac405-195">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ac405-196">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ac405-196">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ac405-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >: listan med språk tillägg.</span><span class="sxs-lookup"><span data-stu-id="ac405-197">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="ac405-198">`[Name <LanguageExtensionName?>]`: Namnet på språk tillägget.</span><span class="sxs-lookup"><span data-stu-id="ac405-198">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="ac405-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: klustrets externa klient organisationer.</span><span class="sxs-lookup"><span data-stu-id="ac405-199">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="ac405-200">`[Value <String>]`: GUID som representerar en extern klient organisation.</span><span class="sxs-lookup"><span data-stu-id="ac405-200">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="ac405-201">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ac405-201">RELATED LINKS</span></span>

