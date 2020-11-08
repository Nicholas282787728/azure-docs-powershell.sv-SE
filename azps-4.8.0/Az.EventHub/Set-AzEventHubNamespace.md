---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: f13a92bef4bfbafc67beec6d99cf02d8d1d63c31
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101006"
---
# <span data-ttu-id="fee1d-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="fee1d-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="fee1d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fee1d-102">SYNOPSIS</span></span>
<span data-ttu-id="fee1d-103">Uppdaterar namn området för de angivna Event Hub.</span><span class="sxs-lookup"><span data-stu-id="fee1d-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="fee1d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fee1d-104">SYNTAX</span></span>

### <span data-ttu-id="fee1d-105">NamespaceParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fee1d-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-Identity] [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fee1d-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="fee1d-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity]
 [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fee1d-107">IdentityUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="fee1d-107">IdentityUpdateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fee1d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fee1d-108">DESCRIPTION</span></span>
<span data-ttu-id="fee1d-109">Set-AzEventHubNamespace cmdlet uppdaterar egenskaperna för de angivna namn områdena för händelse nav.</span><span class="sxs-lookup"><span data-stu-id="fee1d-109">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="fee1d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fee1d-110">EXAMPLES</span></span>

### <span data-ttu-id="fee1d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fee1d-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -Tag @{Tag1='TagValue1'; Tag2='TagValue2'}

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   : {Tag2, TagValue2, Tag1, TagValue1}
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10

```

<span data-ttu-id="fee1d-112">Uppdaterar taggarna för namespace \` MyNamespaceName \` som skapats.</span><span class="sxs-lookup"><span data-stu-id="fee1d-112">Updates the Tags for namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="fee1d-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="fee1d-113">Example 2</span></span>
```powershell
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10 

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroup          : Default-EventHub-WestCentralUS
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="fee1d-114">Uppdaterar tillståndet för namn områdes \` MyNamespaceName \` med automittre = Enabled och MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="fee1d-114">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

### <span data-ttu-id="fee1d-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="fee1d-115">Example 3</span></span>

<span data-ttu-id="fee1d-116">Uppdaterar namn området för de angivna Event Hub.</span><span class="sxs-lookup"><span data-stu-id="fee1d-116">Updates the specified Event Hubs namespace.</span></span> <span data-ttu-id="fee1d-117">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="fee1d-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzEventHubNamespace -Location 'WestUS' -Name MyNamespaceName -ResourceGroupName MyResourceGroupName -SkuName Basic
```

### <span data-ttu-id="fee1d-118">Exempel 5: skapa och uppdatera namnrymd med hantera identitet i ett kluster</span><span class="sxs-lookup"><span data-stu-id="fee1d-118">Example 5: Creating and updating Namespace with Manage Identity in a cluster</span></span> 
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation --EnableAutoInflate -MaximumThroughputUnits 12 -EnableKafka -ZoneRedundant -Identity

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 6/12/2020 4:00:29 AM
UpdatedAt                     : 6/14/2020 11:33:12 PM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 12
ZoneRedundant                 : True
ClusterArmId                  : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/clusters/TestCluster
Identity.PrincipalId          : ##########
Identity.TenantId             : ##########
Identity.Type                 : SystemAssigned
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :

# Get created namespace
PS C:\> $getnamespace = Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName

# Create KeyVault
PS C:\>$Keyvault = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Set Access policy on the KeyVault
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName testingnewCluster -ObjectId $getnamespace.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get -BypassObjectIdValidation

# Add a key to KeyVault
$key = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Update Namespace with KeyVault properties

PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName -Location westus -KeySource Microsoft.KeyVault -KeyProperty @(@($key.Name, $keyvault.VaultUri,""))

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 6/12/2020 4:00:29 AM
UpdatedAt                     : 6/14/2020 11:33:12 PM
ServiceBusEndpoint            : #########
Enabled                       : True
KafkaEnabled                  : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : False
ClusterArmId                  : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/clusters/TestCluster
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          : #########
Identity.TenantId             : #########
Identity.Type                 : SystemAssigned
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          : MicrosoftKeyVault
Encryption.KeyVaultProperties : {testkey, https://myvaultname.vault.azure.net, }
```

## <span data-ttu-id="fee1d-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fee1d-119">PARAMETERS</span></span>

### <span data-ttu-id="fee1d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fee1d-120">-DefaultProfile</span></span>
<span data-ttu-id="fee1d-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fee1d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fee1d-122">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="fee1d-122">-EnableAutoInflate</span></span>
<span data-ttu-id="fee1d-123">Anger om autoöka-funktionen är aktive rad</span><span class="sxs-lookup"><span data-stu-id="fee1d-123">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet, IdentityUpdateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fee1d-124">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="fee1d-124">-EnableKafka</span></span>
<span data-ttu-id="fee1d-125">Aktivera eller inaktivera Kafka för namn områden</span><span class="sxs-lookup"><span data-stu-id="fee1d-125">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="fee1d-126">-Identity</span><span class="sxs-lookup"><span data-stu-id="fee1d-126">-Identity</span></span>
<span data-ttu-id="fee1d-127">Aktivera eller inaktivera identitet för namn område</span><span class="sxs-lookup"><span data-stu-id="fee1d-127">enabling or disabling Identity for namespace</span></span>

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

### <span data-ttu-id="fee1d-128">-IdentityUserDefined</span><span class="sxs-lookup"><span data-stu-id="fee1d-128">-IdentityUserDefined</span></span>
<span data-ttu-id="fee1d-129">Användardefinierad identitet eller ingen</span><span class="sxs-lookup"><span data-stu-id="fee1d-129">User defined Identity or None</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fee1d-130">-Egenskapen-egenskap</span><span class="sxs-lookup"><span data-stu-id="fee1d-130">-KeyProperty</span></span>
<span data-ttu-id="fee1d-131">Lista över egenskaper för nycklar, @ (@ (nyckelvärdet namn, KeyVaultUri, # version), @ (nyckelvärdet, KeyVaultUri, version))</span><span class="sxs-lookup"><span data-stu-id="fee1d-131">List of Key Properties, @(@(KeyName,KeyVaultUri,Keyversion),@(KeyName,KeyVaultUri,Keyversion))</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String[]]
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fee1d-132">-Käll adress</span><span class="sxs-lookup"><span data-stu-id="fee1d-132">-KeySource</span></span>
<span data-ttu-id="fee1d-133">Nyckeltal</span><span class="sxs-lookup"><span data-stu-id="fee1d-133">Key Source</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fee1d-134">-Plats</span><span class="sxs-lookup"><span data-stu-id="fee1d-134">-Location</span></span>
<span data-ttu-id="fee1d-135">Plats för EventHub-namnrymd.</span><span class="sxs-lookup"><span data-stu-id="fee1d-135">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="fee1d-136">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="fee1d-136">-MaximumThroughputUnits</span></span>
<span data-ttu-id="fee1d-137">Övre gräns för flödes enheter när automittre är aktiverat ska värdet vara inom 0 till 20 data flödes enheter.</span><span class="sxs-lookup"><span data-stu-id="fee1d-137">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet, IdentityUpdateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fee1d-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="fee1d-138">-Name</span></span>
<span data-ttu-id="fee1d-139">Namn område för EventHub.</span><span class="sxs-lookup"><span data-stu-id="fee1d-139">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fee1d-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fee1d-140">-ResourceGroupName</span></span>
<span data-ttu-id="fee1d-141">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="fee1d-141">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fee1d-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="fee1d-142">-SkuCapacity</span></span>
<span data-ttu-id="fee1d-143">Eventhub-dataflöden.</span><span class="sxs-lookup"><span data-stu-id="fee1d-143">The eventhub throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fee1d-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fee1d-144">-SkuName</span></span>
<span data-ttu-id="fee1d-145">Namn på SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="fee1d-145">Namespace Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fee1d-146">-State</span><span class="sxs-lookup"><span data-stu-id="fee1d-146">-State</span></span>
<span data-ttu-id="fee1d-147">Inaktivera/aktivera namn område.</span><span class="sxs-lookup"><span data-stu-id="fee1d-147">Disable/Enable Namespace.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.EventHub.Models.NamespaceState]
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fee1d-148">-Tagg</span><span class="sxs-lookup"><span data-stu-id="fee1d-148">-Tag</span></span>
<span data-ttu-id="fee1d-149">Hashtables som representerar en resurs etikett.</span><span class="sxs-lookup"><span data-stu-id="fee1d-149">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fee1d-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fee1d-150">-Confirm</span></span>
<span data-ttu-id="fee1d-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fee1d-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fee1d-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fee1d-152">-WhatIf</span></span>
<span data-ttu-id="fee1d-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fee1d-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fee1d-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fee1d-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fee1d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fee1d-155">CommonParameters</span></span>
<span data-ttu-id="fee1d-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fee1d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fee1d-157">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fee1d-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fee1d-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fee1d-158">INPUTS</span></span>

### <span data-ttu-id="fee1d-159">System. String</span><span class="sxs-lookup"><span data-stu-id="fee1d-159">System.String</span></span>

### <span data-ttu-id="fee1d-160">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="fee1d-160">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="fee1d-161">System. Nullable ' 1 [[Microsoft. Azure. kommandon. EventHub. Models. NamespaceState, Microsoft. Azure. PowerShell. cmdletar. EventHub, version = 1.4.3.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fee1d-161">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.4.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="fee1d-162">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="fee1d-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fee1d-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fee1d-163">OUTPUTS</span></span>

### <span data-ttu-id="fee1d-164">Microsoft. Azure. commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="fee1d-164">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="fee1d-165">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fee1d-165">NOTES</span></span>

## <span data-ttu-id="fee1d-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fee1d-166">RELATED LINKS</span></span>
