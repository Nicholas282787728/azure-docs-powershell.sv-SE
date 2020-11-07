---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: 5717728fa868094a5d1d170af948743d1b9e065b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926141"
---
# <span data-ttu-id="7ae1a-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="7ae1a-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="7ae1a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7ae1a-102">SYNOPSIS</span></span>
<span data-ttu-id="7ae1a-103">Uppdaterar namn området för de angivna Event Hub.</span><span class="sxs-lookup"><span data-stu-id="7ae1a-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="7ae1a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7ae1a-104">SYNTAX</span></span>

### <span data-ttu-id="7ae1a-105">NamespaceParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7ae1a-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ae1a-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ae1a-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ae1a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7ae1a-107">DESCRIPTION</span></span>
<span data-ttu-id="7ae1a-108">Set-AzEventHubNamespace cmdlet uppdaterar egenskaperna för de angivna namn områdena för händelse nav.</span><span class="sxs-lookup"><span data-stu-id="7ae1a-108">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="7ae1a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7ae1a-109">EXAMPLES</span></span>

### <span data-ttu-id="7ae1a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7ae1a-110">Example 1</span></span>
```
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

<span data-ttu-id="7ae1a-111">Uppdaterar taggarna för namespace \` MyNamespaceName \` som skapats.</span><span class="sxs-lookup"><span data-stu-id="7ae1a-111">Updates the Tags for namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="7ae1a-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7ae1a-112">Example 2</span></span>
```
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

<span data-ttu-id="7ae1a-113">Uppdaterar tillståndet för namn områdes \` MyNamespaceName \` med automittre = Enabled och MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="7ae1a-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="7ae1a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7ae1a-114">PARAMETERS</span></span>

### <span data-ttu-id="7ae1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ae1a-115">-DefaultProfile</span></span>
<span data-ttu-id="7ae1a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7ae1a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ae1a-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="7ae1a-117">-EnableAutoInflate</span></span>
<span data-ttu-id="7ae1a-118">Anger om autoöka-funktionen är aktive rad</span><span class="sxs-lookup"><span data-stu-id="7ae1a-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="7ae1a-119">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="7ae1a-119">-EnableKafka</span></span>
<span data-ttu-id="7ae1a-120">Aktivera eller inaktivera Kafka för namn områden</span><span class="sxs-lookup"><span data-stu-id="7ae1a-120">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="7ae1a-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="7ae1a-121">-Location</span></span>
<span data-ttu-id="7ae1a-122">Plats för EventHub-namnrymd.</span><span class="sxs-lookup"><span data-stu-id="7ae1a-122">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="7ae1a-123">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="7ae1a-123">-MaximumThroughputUnits</span></span>
<span data-ttu-id="7ae1a-124">Övre gräns för flödes enheter när automittre är aktiverat ska värdet vara inom 0 till 20 data flödes enheter.</span><span class="sxs-lookup"><span data-stu-id="7ae1a-124">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae1a-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="7ae1a-125">-Name</span></span>
<span data-ttu-id="7ae1a-126">Namn område för EventHub.</span><span class="sxs-lookup"><span data-stu-id="7ae1a-126">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="7ae1a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ae1a-127">-ResourceGroupName</span></span>
<span data-ttu-id="7ae1a-128">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="7ae1a-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="7ae1a-129">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="7ae1a-129">-SkuCapacity</span></span>
<span data-ttu-id="7ae1a-130">Eventhub-dataflöden.</span><span class="sxs-lookup"><span data-stu-id="7ae1a-130">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="7ae1a-131">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7ae1a-131">-SkuName</span></span>
<span data-ttu-id="7ae1a-132">Namn på SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="7ae1a-132">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="7ae1a-133">-State</span><span class="sxs-lookup"><span data-stu-id="7ae1a-133">-State</span></span>
<span data-ttu-id="7ae1a-134">Inaktivera/aktivera namn område.</span><span class="sxs-lookup"><span data-stu-id="7ae1a-134">Disable/Enable Namespace.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.EventHub.Models.NamespaceState]
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae1a-135">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7ae1a-135">-Tag</span></span>
<span data-ttu-id="7ae1a-136">Hashtables som representerar en resurs etikett.</span><span class="sxs-lookup"><span data-stu-id="7ae1a-136">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="7ae1a-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7ae1a-137">-Confirm</span></span>
<span data-ttu-id="7ae1a-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7ae1a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ae1a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ae1a-139">-WhatIf</span></span>
<span data-ttu-id="7ae1a-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7ae1a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ae1a-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7ae1a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ae1a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ae1a-142">CommonParameters</span></span>
<span data-ttu-id="7ae1a-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ae1a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ae1a-144">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ae1a-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ae1a-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7ae1a-145">INPUTS</span></span>

### <span data-ttu-id="7ae1a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="7ae1a-146">System.String</span></span>

### <span data-ttu-id="7ae1a-147">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7ae1a-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7ae1a-148">System. Nullable ' 1 [[Microsoft. Azure. kommandon. EventHub. Models. NamespaceState, Microsoft. Azure. PowerShell. cmdletar. EventHub, version = 1.3.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7ae1a-148">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="7ae1a-149">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="7ae1a-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7ae1a-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7ae1a-150">OUTPUTS</span></span>

### <span data-ttu-id="7ae1a-151">Microsoft. Azure. commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="7ae1a-151">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="7ae1a-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7ae1a-152">NOTES</span></span>

## <span data-ttu-id="7ae1a-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7ae1a-153">RELATED LINKS</span></span>
