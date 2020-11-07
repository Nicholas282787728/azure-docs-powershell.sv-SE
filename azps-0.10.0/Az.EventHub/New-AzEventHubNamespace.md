---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: 592af2c1ecd26e3e744845ae24e8f9c71cf0b0f3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922890"
---
# <span data-ttu-id="5eae5-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="5eae5-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="5eae5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5eae5-102">SYNOPSIS</span></span>
<span data-ttu-id="5eae5-103">Skapar ett namn område för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="5eae5-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="5eae5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5eae5-104">SYNTAX</span></span>

### <span data-ttu-id="5eae5-105">NamespaceParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5eae5-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5eae5-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="5eae5-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5eae5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5eae5-107">DESCRIPTION</span></span>
<span data-ttu-id="5eae5-108">New-AzEventHubNamespace-cmdleten skapar ett nytt namn område av typen Event Hub.</span><span class="sxs-lookup"><span data-stu-id="5eae5-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="5eae5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5eae5-109">EXAMPLES</span></span>

### <span data-ttu-id="5eae5-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5eae5-110">Example 1</span></span>                                           
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
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
IsAutoInflateEnabled   : False
MaximumThroughputUnits : 0
```

<span data-ttu-id="5eae5-111">Skapar en namnrymd för händelse nav \` MyNamespaceName \` på min plats med geografisk plats \` \` i MyResourceGroupName för resurs \` grupp \` .</span><span class="sxs-lookup"><span data-stu-id="5eae5-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="5eae5-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5eae5-112">Example 2</span></span>
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
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
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="5eae5-113">Skapar namn områdes \` MyNamespaceName för Event Hub \` på den angivna geografiska platsen min \` plats \` , i resurs grupp \` MyResourceGroupName \` och automittre är aktiverat med MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="5eae5-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="5eae5-114">Exempel 3 – Kafka aktiverat namn område</span><span class="sxs-lookup"><span data-stu-id="5eae5-114">Example 3 - Kafka enabled namespace</span></span>
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
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
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 12
```

<span data-ttu-id="5eae5-115">Skapar ett namn område för händelse nav \` MyNamespaceName \` på den angivna geografiska platsen min \` plats \` , i resurs grupp \` MyResourceGroupName \` med Kafka och automittre aktiverat.</span><span class="sxs-lookup"><span data-stu-id="5eae5-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

## <span data-ttu-id="5eae5-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5eae5-116">PARAMETERS</span></span>

### <span data-ttu-id="5eae5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eae5-117">-DefaultProfile</span></span>
<span data-ttu-id="5eae5-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5eae5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5eae5-119">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="5eae5-119">-EnableAutoInflate</span></span>
<span data-ttu-id="5eae5-120">Anger om autoöka-funktionen är aktive rad</span><span class="sxs-lookup"><span data-stu-id="5eae5-120">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="5eae5-121">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="5eae5-121">-EnableKafka</span></span>
<span data-ttu-id="5eae5-122">Aktivera eller inaktivera Kafka för namn områden</span><span class="sxs-lookup"><span data-stu-id="5eae5-122">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="5eae5-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="5eae5-123">-Location</span></span>
<span data-ttu-id="5eae5-124">Plats för EventHub-namnrymd.</span><span class="sxs-lookup"><span data-stu-id="5eae5-124">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="5eae5-125">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="5eae5-125">-MaximumThroughputUnits</span></span>
<span data-ttu-id="5eae5-126">Övre gräns för flödes enheter när automittre är aktiverat ska värdet vara inom 0 till 20 data flödes enheter.</span><span class="sxs-lookup"><span data-stu-id="5eae5-126">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="5eae5-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="5eae5-127">-Name</span></span>
<span data-ttu-id="5eae5-128">Namn område för EventHub.</span><span class="sxs-lookup"><span data-stu-id="5eae5-128">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="5eae5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eae5-129">-ResourceGroupName</span></span>
<span data-ttu-id="5eae5-130">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="5eae5-130">Resource Group Name</span></span>

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

### <span data-ttu-id="5eae5-131">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="5eae5-131">-SkuCapacity</span></span>
<span data-ttu-id="5eae5-132">Eventhub-dataflöden.</span><span class="sxs-lookup"><span data-stu-id="5eae5-132">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="5eae5-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5eae5-133">-SkuName</span></span>
<span data-ttu-id="5eae5-134">Namn på SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="5eae5-134">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="5eae5-135">-Tagg</span><span class="sxs-lookup"><span data-stu-id="5eae5-135">-Tag</span></span>
<span data-ttu-id="5eae5-136">Hashtables som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="5eae5-136">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="5eae5-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5eae5-137">-Confirm</span></span>
<span data-ttu-id="5eae5-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5eae5-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5eae5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5eae5-139">-WhatIf</span></span>
<span data-ttu-id="5eae5-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5eae5-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5eae5-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5eae5-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5eae5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eae5-142">CommonParameters</span></span>
<span data-ttu-id="5eae5-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eae5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eae5-144">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5eae5-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eae5-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5eae5-145">INPUTS</span></span>

### <span data-ttu-id="5eae5-146">System. String</span><span class="sxs-lookup"><span data-stu-id="5eae5-146">System.String</span></span>

### <span data-ttu-id="5eae5-147">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5eae5-147">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5eae5-148">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="5eae5-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5eae5-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5eae5-149">OUTPUTS</span></span>

### <span data-ttu-id="5eae5-150">Microsoft. Azure. commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="5eae5-150">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="5eae5-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5eae5-151">NOTES</span></span>

## <span data-ttu-id="5eae5-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5eae5-152">RELATED LINKS</span></span>
