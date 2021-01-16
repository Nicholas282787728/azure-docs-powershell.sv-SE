---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: b8b6c11da622b7fa0ee67dc418f2055dd72c1d13
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410232"
---
# <span data-ttu-id="ddadf-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="ddadf-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="ddadf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ddadf-102">SYNOPSIS</span></span>
<span data-ttu-id="ddadf-103">Skapa eller uppdatera ett Kusto-kluster.</span><span class="sxs-lookup"><span data-stu-id="ddadf-103">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="ddadf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ddadf-104">SYNTAX</span></span>

```
New-AzKustoCluster -Name <String> -ResourceGroupName <String> -Location <String> -SkuName <AzureSkuName>
 -SkuTier <AzureSkuTier> [-SubscriptionId <String>] [-EnableDiskEncryption] [-EnableDoubleEncryption]
 [-EnablePurge] [-EnableStreamingIngest] [-IdentityType <IdentityType>]
 [-IdentityUserAssignedIdentity <Hashtable>] [-KeyVaultPropertyKeyName <String>]
 [-KeyVaultPropertyKeyVaultUri <String>] [-KeyVaultPropertyKeyVersion <String>]
 [-LanguageExtensionValue <ILanguageExtension[]>] [-OptimizedAutoscaleIsEnabled]
 [-OptimizedAutoscaleMaximum <Int32>] [-OptimizedAutoscaleMinimum <Int32>]
 [-OptimizedAutoscaleVersion <Int32>] [-SkuCapacity <Int32>] [-Tag <Hashtable>]
 [-TrustedExternalTenant <ITrustedExternalTenant[]>]
 [-VirtualNetworkConfigurationDataManagementPublicIPId <String>]
 [-VirtualNetworkConfigurationEnginePublicIPId <String>] [-VirtualNetworkConfigurationSubnetId <String>]
 [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ddadf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ddadf-105">DESCRIPTION</span></span>
<span data-ttu-id="ddadf-106">Skapa eller uppdatera ett Kusto-kluster.</span><span class="sxs-lookup"><span data-stu-id="ddadf-106">Create or update a Kusto cluster.</span></span>

## <span data-ttu-id="ddadf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ddadf-107">EXAMPLES</span></span>

### <span data-ttu-id="ddadf-108">Exempel 1: skapa ett nytt Kusto-kluster</span><span class="sxs-lookup"><span data-stu-id="ddadf-108">Example 1: Create a new Kusto cluster</span></span>
```powershell
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster -Location 'East US' -SkuName Standard_D11_v2 -SkuTier Standard -EnableDoubleEncryption true

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="ddadf-109">Med kommandot ovan skapas ett nytt Kusto-kluster med namnet "testnewkustocluster" i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="ddadf-109">The above command creates a new Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="ddadf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ddadf-110">PARAMETERS</span></span>

### <span data-ttu-id="ddadf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddadf-111">-AsJob</span></span>
<span data-ttu-id="ddadf-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="ddadf-112">Run the command as a job</span></span>

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

### <span data-ttu-id="ddadf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddadf-113">-DefaultProfile</span></span>
<span data-ttu-id="ddadf-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ddadf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddadf-115">-EnableDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="ddadf-115">-EnableDiskEncryption</span></span>
<span data-ttu-id="ddadf-116">Ett booleskt värde som anger om klustrets diskar är krypterade.</span><span class="sxs-lookup"><span data-stu-id="ddadf-116">A boolean value that indicates if the cluster's disks are encrypted.</span></span>

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

### <span data-ttu-id="ddadf-117">-EnableDoubleEncryption</span><span class="sxs-lookup"><span data-stu-id="ddadf-117">-EnableDoubleEncryption</span></span>
<span data-ttu-id="ddadf-118">Ett booleskt värde som anger om Double Encryption är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="ddadf-118">A boolean value that indicates if double encryption is enabled.</span></span>

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

### <span data-ttu-id="ddadf-119">-EnablePurge</span><span class="sxs-lookup"><span data-stu-id="ddadf-119">-EnablePurge</span></span>
<span data-ttu-id="ddadf-120">Ett booleskt värde som anger om rensningen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="ddadf-120">A boolean value that indicates if the purge operations are enabled.</span></span>

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

### <span data-ttu-id="ddadf-121">-EnableStreamingIngest</span><span class="sxs-lookup"><span data-stu-id="ddadf-121">-EnableStreamingIngest</span></span>
<span data-ttu-id="ddadf-122">Ett booleskt värde som anger om streaming-funktionen är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="ddadf-122">A boolean value that indicates if the streaming ingest is enabled.</span></span>

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

### <span data-ttu-id="ddadf-123">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="ddadf-123">-IdentityType</span></span>
<span data-ttu-id="ddadf-124">Identitets typen.</span><span class="sxs-lookup"><span data-stu-id="ddadf-124">The identity type.</span></span>

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

### <span data-ttu-id="ddadf-125">-IdentityUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ddadf-125">-IdentityUserAssignedIdentity</span></span>
<span data-ttu-id="ddadf-126">Listan över användar identiteter som är kopplade till Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="ddadf-126">The list of user identities associated with the Kusto cluster.</span></span>
<span data-ttu-id="ddadf-127">Nyckelorden för användar identitets ord lista är ARM resurs-ID i formatet: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} '.</span><span class="sxs-lookup"><span data-stu-id="ddadf-127">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="ddadf-128">-KeyVaultPropertyKeyName</span><span class="sxs-lookup"><span data-stu-id="ddadf-128">-KeyVaultPropertyKeyName</span></span>
<span data-ttu-id="ddadf-129">Namnet på Key valv-tangenten.</span><span class="sxs-lookup"><span data-stu-id="ddadf-129">The name of the key vault key.</span></span>

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

### <span data-ttu-id="ddadf-130">-KeyVaultPropertyKeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="ddadf-130">-KeyVaultPropertyKeyVaultUri</span></span>
<span data-ttu-id="ddadf-131">URI för Key Vault.</span><span class="sxs-lookup"><span data-stu-id="ddadf-131">The Uri of the key vault.</span></span>

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

### <span data-ttu-id="ddadf-132">-KeyVaultPropertyKeyVersion</span><span class="sxs-lookup"><span data-stu-id="ddadf-132">-KeyVaultPropertyKeyVersion</span></span>
<span data-ttu-id="ddadf-133">Versionen av Key valv-tangenten.</span><span class="sxs-lookup"><span data-stu-id="ddadf-133">The version of the key vault key.</span></span>

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

### <span data-ttu-id="ddadf-134">-LanguageExtensionValue</span><span class="sxs-lookup"><span data-stu-id="ddadf-134">-LanguageExtensionValue</span></span>
<span data-ttu-id="ddadf-135">Listan över språk tillägg.</span><span class="sxs-lookup"><span data-stu-id="ddadf-135">The list of language extensions.</span></span>
<span data-ttu-id="ddadf-136">För att konstruera kan du läsa avsnittet anteckningar för LANGUAGEEXTENSIONVALUE-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="ddadf-136">To construct, see NOTES section for LANGUAGEEXTENSIONVALUE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ddadf-137">-Plats</span><span class="sxs-lookup"><span data-stu-id="ddadf-137">-Location</span></span>
<span data-ttu-id="ddadf-138">Den Geo-plats där resursen bor</span><span class="sxs-lookup"><span data-stu-id="ddadf-138">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="ddadf-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="ddadf-139">-Name</span></span>
<span data-ttu-id="ddadf-140">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="ddadf-140">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ddadf-141">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ddadf-141">-NoWait</span></span>
<span data-ttu-id="ddadf-142">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="ddadf-142">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ddadf-143">-OptimizedAutoscaleIsEnabled</span><span class="sxs-lookup"><span data-stu-id="ddadf-143">-OptimizedAutoscaleIsEnabled</span></span>
<span data-ttu-id="ddadf-144">Ett booleskt värde som anger om den optimerade autoskalningsfunktionen är aktive rad eller inte.</span><span class="sxs-lookup"><span data-stu-id="ddadf-144">A boolean value that indicate if the optimized autoscale feature is enabled or not.</span></span>

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

### <span data-ttu-id="ddadf-145">-OptimizedAutoscaleMaximum</span><span class="sxs-lookup"><span data-stu-id="ddadf-145">-OptimizedAutoscaleMaximum</span></span>
<span data-ttu-id="ddadf-146">Maximalt antal tillåtna instanser.</span><span class="sxs-lookup"><span data-stu-id="ddadf-146">Maximum allowed instances count.</span></span>

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

### <span data-ttu-id="ddadf-147">-OptimizedAutoscaleMinimum</span><span class="sxs-lookup"><span data-stu-id="ddadf-147">-OptimizedAutoscaleMinimum</span></span>
<span data-ttu-id="ddadf-148">Antal tillåtna instanser.</span><span class="sxs-lookup"><span data-stu-id="ddadf-148">Minimum allowed instances count.</span></span>

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

### <span data-ttu-id="ddadf-149">-OptimizedAutoscaleVersion</span><span class="sxs-lookup"><span data-stu-id="ddadf-149">-OptimizedAutoscaleVersion</span></span>
<span data-ttu-id="ddadf-150">Versionen av den definierade mallen, till exempel 1.</span><span class="sxs-lookup"><span data-stu-id="ddadf-150">The version of the template defined, for instance 1.</span></span>

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

### <span data-ttu-id="ddadf-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddadf-151">-ResourceGroupName</span></span>
<span data-ttu-id="ddadf-152">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="ddadf-152">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ddadf-153">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ddadf-153">-SkuCapacity</span></span>
<span data-ttu-id="ddadf-154">Antalet instanser av klustret.</span><span class="sxs-lookup"><span data-stu-id="ddadf-154">The number of instances of the cluster.</span></span>

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

### <span data-ttu-id="ddadf-155">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ddadf-155">-SkuName</span></span>
<span data-ttu-id="ddadf-156">SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="ddadf-156">SKU name.</span></span>

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

### <span data-ttu-id="ddadf-157">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ddadf-157">-SkuTier</span></span>
<span data-ttu-id="ddadf-158">SKU-nivå.</span><span class="sxs-lookup"><span data-stu-id="ddadf-158">SKU tier.</span></span>

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

### <span data-ttu-id="ddadf-159">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ddadf-159">-SubscriptionId</span></span>
<span data-ttu-id="ddadf-160">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="ddadf-160">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ddadf-161">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="ddadf-161">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ddadf-162">-Tagg</span><span class="sxs-lookup"><span data-stu-id="ddadf-162">-Tag</span></span>
<span data-ttu-id="ddadf-163">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="ddadf-163">Resource tags.</span></span>

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

### <span data-ttu-id="ddadf-164">-TrustedExternalTenant</span><span class="sxs-lookup"><span data-stu-id="ddadf-164">-TrustedExternalTenant</span></span>
<span data-ttu-id="ddadf-165">Klustrets externa klient organisationer.</span><span class="sxs-lookup"><span data-stu-id="ddadf-165">The cluster's external tenants.</span></span>
<span data-ttu-id="ddadf-166">För att konstruera kan du läsa avsnittet anteckningar för TRUSTEDEXTERNALTENANT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="ddadf-166">To construct, see NOTES section for TRUSTEDEXTERNALTENANT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ddadf-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span><span class="sxs-lookup"><span data-stu-id="ddadf-167">-VirtualNetworkConfigurationDataManagementPublicIPId</span></span>
<span data-ttu-id="ddadf-168">Resurs-ID för offentlig IP-adress för data hantering.</span><span class="sxs-lookup"><span data-stu-id="ddadf-168">Data management's service public IP address resource id.</span></span>

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

### <span data-ttu-id="ddadf-169">-VirtualNetworkConfigurationEnginePublicIPId</span><span class="sxs-lookup"><span data-stu-id="ddadf-169">-VirtualNetworkConfigurationEnginePublicIPId</span></span>
<span data-ttu-id="ddadf-170">Motor tjänstens resurs-ID för offentlig IP-adress.</span><span class="sxs-lookup"><span data-stu-id="ddadf-170">Engine service's public IP address resource id.</span></span>

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

### <span data-ttu-id="ddadf-171">-VirtualNetworkConfigurationSubnetId</span><span class="sxs-lookup"><span data-stu-id="ddadf-171">-VirtualNetworkConfigurationSubnetId</span></span>
<span data-ttu-id="ddadf-172">ID för under nätets resurs.</span><span class="sxs-lookup"><span data-stu-id="ddadf-172">The subnet resource id.</span></span>

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

### <span data-ttu-id="ddadf-173">-Zone</span><span class="sxs-lookup"><span data-stu-id="ddadf-173">-Zone</span></span>
<span data-ttu-id="ddadf-174">Klustrets tillgänglighets zoner.</span><span class="sxs-lookup"><span data-stu-id="ddadf-174">The availability zones of the cluster.</span></span>

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

### <span data-ttu-id="ddadf-175">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ddadf-175">-Confirm</span></span>
<span data-ttu-id="ddadf-176">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ddadf-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddadf-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddadf-177">-WhatIf</span></span>
<span data-ttu-id="ddadf-178">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ddadf-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddadf-179">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ddadf-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddadf-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddadf-180">CommonParameters</span></span>
<span data-ttu-id="ddadf-181">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddadf-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddadf-182">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddadf-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddadf-183">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ddadf-183">INPUTS</span></span>

## <span data-ttu-id="ddadf-184">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ddadf-184">OUTPUTS</span></span>

### <span data-ttu-id="ddadf-185">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. ICluster</span><span class="sxs-lookup"><span data-stu-id="ddadf-185">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="ddadf-186">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ddadf-186">NOTES</span></span>

<span data-ttu-id="ddadf-187">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ddadf-187">ALIASES</span></span>

<span data-ttu-id="ddadf-188">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="ddadf-188">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ddadf-189">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="ddadf-189">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ddadf-190">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ddadf-190">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ddadf-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension [] >: listan med språk tillägg.</span><span class="sxs-lookup"><span data-stu-id="ddadf-191">LANGUAGEEXTENSIONVALUE <ILanguageExtension[]>: The list of language extensions.</span></span>
  - <span data-ttu-id="ddadf-192">`[Name <LanguageExtensionName?>]`: Namnet på språk tillägget.</span><span class="sxs-lookup"><span data-stu-id="ddadf-192">`[Name <LanguageExtensionName?>]`: The language extension name.</span></span>

<span data-ttu-id="ddadf-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant [] >: klustrets externa klient organisationer.</span><span class="sxs-lookup"><span data-stu-id="ddadf-193">TRUSTEDEXTERNALTENANT <ITrustedExternalTenant[]>: The cluster's external tenants.</span></span>
  - <span data-ttu-id="ddadf-194">`[Value <String>]`: GUID som representerar en extern klient organisation.</span><span class="sxs-lookup"><span data-stu-id="ddadf-194">`[Value <String>]`: GUID representing an external tenant.</span></span>

## <span data-ttu-id="ddadf-195">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ddadf-195">RELATED LINKS</span></span>

