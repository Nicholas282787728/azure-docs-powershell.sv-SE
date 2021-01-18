---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: a51fffe36102b05121e52054103357bd26f56d51
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523683"
---
# <span data-ttu-id="17dfa-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="17dfa-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="17dfa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="17dfa-102">SYNOPSIS</span></span>
<span data-ttu-id="17dfa-103">Skapar ett namn område för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="17dfa-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="17dfa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="17dfa-104">SYNTAX</span></span>

### <span data-ttu-id="17dfa-105">NamespaceParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="17dfa-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka] [-ZoneRedundant]
 [[-ClusterARMId] <String>] [-Identity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="17dfa-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="17dfa-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-ZoneRedundant] [[-ClusterARMId] <String>] [-Identity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17dfa-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="17dfa-107">DESCRIPTION</span></span>
<span data-ttu-id="17dfa-108">New-AzEventHubNamespace-cmdleten skapar ett nytt namn område av typen Event Hub.</span><span class="sxs-lookup"><span data-stu-id="17dfa-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="17dfa-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="17dfa-109">EXAMPLES</span></span>
### <span data-ttu-id="17dfa-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="17dfa-110">Example 1</span></span>                                           
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 6/14/2020 9:02:16 PM
UpdatedAt                     : 6/14/2020 9:03:04 PM
ServiceBusEndpoint            : https://testingnew2018.servicebus.windows.net:443/
Enabled                       : True
KafkaEnabled                  : True
IsAutoInflateEnabled          : False
MaximumThroughputUnits        : 0
ZoneRedundant                 : False
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="17dfa-111">Skapar en namnrymd för händelse nav \` MyNamespaceName \` på min plats med geografisk plats \` \` i MyResourceGroupName för resurs \` grupp \` .</span><span class="sxs-lookup"><span data-stu-id="17dfa-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="17dfa-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="17dfa-112">Example 2</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : False
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="17dfa-113">Skapar namn områdes \` MyNamespaceName för Event Hub \` på den angivna geografiska platsen min \` plats \` , i resurs grupp \` MyResourceGroupName \` och automittre är aktiverat med MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="17dfa-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="17dfa-114">Exempel 3: Kafka aktive rad namnrymd</span><span class="sxs-lookup"><span data-stu-id="17dfa-114">Example 3: Kafka enabled namespace</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : False
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="17dfa-115">Skapar ett namn område för händelse nav \` MyNamespaceName \` på den angivna geografiska platsen min \` plats \` , i resurs grupp \` MyResourceGroupName \` med Kafka och automittre aktiverat.</span><span class="sxs-lookup"><span data-stu-id="17dfa-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

### <span data-ttu-id="17dfa-116">Exempel 4: ZoneRedundant aktive rad namnrymd</span><span class="sxs-lookup"><span data-stu-id="17dfa-116">Example 4: ZoneRedundant enabled namespace</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -ZoneRedundant

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : True
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="17dfa-117">Skapar ett namn område för händelse nav \` MyNamespaceName \` på den angivna geografiska platsen min \` plats \` , i resurs grupp \` MyResourceGroupName \` med Kafka och automittre aktiverat.</span><span class="sxs-lookup"><span data-stu-id="17dfa-117">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

### <span data-ttu-id="17dfa-118">Exempel 5: skapa namnrymd med hantera identitet i ett kluster</span><span class="sxs-lookup"><span data-stu-id="17dfa-118">Example 5: Creating Namespace with Manage Identity in a cluster</span></span> 
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
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
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
PS C:\>$getnamespace = Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName

# Create KeyVault
PS C:\>$Keyvault = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Set Access policy on the KeyVault
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName testingnewCluster -ObjectId $getnamespace.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get -BypassObjectIdValidation

# Add a key to KeyVault
PS C:\> $key = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Update Namespace with KeyVault properties

PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName -Location westus -KeySource Microsoft.KeyVault -KeyProperties @(@($key.Name, $keyvault.VaultUri,""))

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

## <span data-ttu-id="17dfa-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="17dfa-119">PARAMETERS</span></span>

### <span data-ttu-id="17dfa-120">-ClusterARMId</span><span class="sxs-lookup"><span data-stu-id="17dfa-120">-ClusterARMId</span></span>
<span data-ttu-id="17dfa-121">ARM-ID för kluster där namn område ska skapas</span><span class="sxs-lookup"><span data-stu-id="17dfa-121">ARM ID of Cluster where namespace is to be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17dfa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17dfa-122">-DefaultProfile</span></span>
<span data-ttu-id="17dfa-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="17dfa-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17dfa-124">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="17dfa-124">-EnableAutoInflate</span></span>
<span data-ttu-id="17dfa-125">Anger om autoöka-funktionen är aktive rad</span><span class="sxs-lookup"><span data-stu-id="17dfa-125">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17dfa-126">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="17dfa-126">-EnableKafka</span></span>
<span data-ttu-id="17dfa-127">Aktivera eller inaktivera Kafka för namn områden</span><span class="sxs-lookup"><span data-stu-id="17dfa-127">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="17dfa-128">-Identity</span><span class="sxs-lookup"><span data-stu-id="17dfa-128">-Identity</span></span>
<span data-ttu-id="17dfa-129">Aktivera eller inaktivera identitet för namn område</span><span class="sxs-lookup"><span data-stu-id="17dfa-129">enabling or disabling Identity for namespace</span></span>

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

### <span data-ttu-id="17dfa-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="17dfa-130">-Location</span></span>
<span data-ttu-id="17dfa-131">Plats för EventHub-namnrymd.</span><span class="sxs-lookup"><span data-stu-id="17dfa-131">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="17dfa-132">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="17dfa-132">-MaximumThroughputUnits</span></span>
<span data-ttu-id="17dfa-133">Övre gräns för flödes enheter när automittre är aktiverat ska värdet vara inom 0 till 20 data flödes enheter.</span><span class="sxs-lookup"><span data-stu-id="17dfa-133">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17dfa-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="17dfa-134">-Name</span></span>
<span data-ttu-id="17dfa-135">Namn område för EventHub.</span><span class="sxs-lookup"><span data-stu-id="17dfa-135">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="17dfa-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17dfa-136">-ResourceGroupName</span></span>
<span data-ttu-id="17dfa-137">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="17dfa-137">Resource Group Name</span></span>

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

### <span data-ttu-id="17dfa-138">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="17dfa-138">-SkuCapacity</span></span>
<span data-ttu-id="17dfa-139">Eventhub-dataflöden.</span><span class="sxs-lookup"><span data-stu-id="17dfa-139">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="17dfa-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="17dfa-140">-SkuName</span></span>
<span data-ttu-id="17dfa-141">Namn på SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="17dfa-141">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="17dfa-142">-Tagg</span><span class="sxs-lookup"><span data-stu-id="17dfa-142">-Tag</span></span>
<span data-ttu-id="17dfa-143">Hashtables som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="17dfa-143">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17dfa-144">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="17dfa-144">-ZoneRedundant</span></span>
<span data-ttu-id="17dfa-145">Aktivera eller inaktivera zonens redundant för namn område</span><span class="sxs-lookup"><span data-stu-id="17dfa-145">enabling or disabling Zone Redundant for namespace</span></span>

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

### <span data-ttu-id="17dfa-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="17dfa-146">-Confirm</span></span>
<span data-ttu-id="17dfa-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="17dfa-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17dfa-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17dfa-148">-WhatIf</span></span>
<span data-ttu-id="17dfa-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="17dfa-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17dfa-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="17dfa-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17dfa-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17dfa-151">CommonParameters</span></span>
<span data-ttu-id="17dfa-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17dfa-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17dfa-153">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17dfa-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17dfa-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="17dfa-154">INPUTS</span></span>

### <span data-ttu-id="17dfa-155">System. String</span><span class="sxs-lookup"><span data-stu-id="17dfa-155">System.String</span></span>

### <span data-ttu-id="17dfa-156">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="17dfa-156">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="17dfa-157">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="17dfa-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="17dfa-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="17dfa-158">OUTPUTS</span></span>

### <span data-ttu-id="17dfa-159">Microsoft. Azure. commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="17dfa-159">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="17dfa-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="17dfa-160">NOTES</span></span>

## <span data-ttu-id="17dfa-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="17dfa-161">RELATED LINKS</span></span>
