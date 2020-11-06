---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/6911f050bfba3248a3fd992fbc2645e3a1a8641d
ms.openlocfilehash: 05f0c3cd3947a1955689a7359b40d59052863ce1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574669"
---
# <span data-ttu-id="27b6c-101">Set-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="27b6c-101">Set-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="27b6c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="27b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="27b6c-103">Uppdaterar namn området för de angivna Event Hub.</span><span class="sxs-lookup"><span data-stu-id="27b6c-103">Updates the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27b6c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="27b6c-104">SYNTAX</span></span>

### <span data-ttu-id="27b6c-105">NamespaceParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="27b6c-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="27b6c-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="27b6c-106">AutoInflateParameterSet</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="27b6c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="27b6c-107">DESCRIPTION</span></span>
<span data-ttu-id="27b6c-108">Set-AzureRmEventHubNamespace cmdlet uppdaterar egenskaperna för de angivna namn områdena för händelse nav.</span><span class="sxs-lookup"><span data-stu-id="27b6c-108">The Set-AzureRmEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="27b6c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="27b6c-109">EXAMPLES</span></span>

### <span data-ttu-id="27b6c-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="27b6c-110">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="27b6c-111">Uppdaterar tillståndet för namespace \` MyNamespaceName \` till skapad.</span><span class="sxs-lookup"><span data-stu-id="27b6c-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="27b6c-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="27b6c-112">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="27b6c-113">Uppdaterar tillståndet för namn områdes \` MyNamespaceName \` med automittre = Enabled och MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="27b6c-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="27b6c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="27b6c-114">PARAMETERS</span></span>

### <span data-ttu-id="27b6c-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="27b6c-115">-Location</span></span>
<span data-ttu-id="27b6c-116">Namn område för händelse nav Geo-Location.</span><span class="sxs-lookup"><span data-stu-id="27b6c-116">Event Hubs namespace geo-location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b6c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27b6c-117">-ResourceGroupName</span></span>
<span data-ttu-id="27b6c-118">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="27b6c-118">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b6c-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="27b6c-119">-SkuCapacity</span></span>
<span data-ttu-id="27b6c-120">Data flödes enheter för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="27b6c-120">The Event Hub throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b6c-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="27b6c-121">-SkuName</span></span>
<span data-ttu-id="27b6c-122">Namn på SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="27b6c-122">Namespace Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b6c-123">-State</span><span class="sxs-lookup"><span data-stu-id="27b6c-123">-State</span></span>
<span data-ttu-id="27b6c-124">Anger tillstånd (inaktiverat eller aktiverat) för namn området.</span><span class="sxs-lookup"><span data-stu-id="27b6c-124">Specifies the state (disabled or enabled) of the namespace.</span></span>

```yaml
Type: NamespaceState
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, Creating, Created, Activating, Enabling, Active, Disabling, Disabled, SoftDeleting, SoftDeleted, Removing, Removed, Failed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b6c-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="27b6c-125">-Tag</span></span>
<span data-ttu-id="27b6c-126">Hashtables som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="27b6c-126">Hashtables that represent resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b6c-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="27b6c-127">-Confirm</span></span>
<span data-ttu-id="27b6c-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="27b6c-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b6c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27b6c-129">-WhatIf</span></span>
<span data-ttu-id="27b6c-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="27b6c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27b6c-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="27b6c-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b6c-132">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="27b6c-132">-EnableAutoInflate</span></span>
<span data-ttu-id="27b6c-133">Anger om autoöka-funktionen är aktive rad</span><span class="sxs-lookup"><span data-stu-id="27b6c-133">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: NamespaceParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b6c-134">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="27b6c-134">-MaximumThroughputUnits</span></span>
<span data-ttu-id="27b6c-135">Övre gräns för flödes enheter när automittre är aktiverat ska Vaule vara inom 0 till 20 data flödes enheter.</span><span class="sxs-lookup"><span data-stu-id="27b6c-135">Upper limit of throughput units when AutoInflate is enabled, vaule should be within 0 to 20 throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b6c-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="27b6c-136">-Name</span></span>
<span data-ttu-id="27b6c-137">Namn område för EventHub.</span><span class="sxs-lookup"><span data-stu-id="27b6c-137">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="27b6c-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="27b6c-138">INPUTS</span></span>

### <span data-ttu-id="27b6c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="27b6c-139">System.String</span></span>

### <span data-ttu-id="27b6c-140">System. Int32</span><span class="sxs-lookup"><span data-stu-id="27b6c-140">System.Int32</span></span>

### <span data-ttu-id="27b6c-141">Microsoft. Azure. Management. EventHub. Models. NamespaceState</span><span class="sxs-lookup"><span data-stu-id="27b6c-141">Microsoft.Azure.Management.EventHub.Models.NamespaceState</span></span>

### <span data-ttu-id="27b6c-142">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="27b6c-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="27b6c-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="27b6c-143">OUTPUTS</span></span>

### <span data-ttu-id="27b6c-144">Microsoft. Azure. commands. EventHub. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="27b6c-144">Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="27b6c-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="27b6c-145">NOTES</span></span>

## <span data-ttu-id="27b6c-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="27b6c-146">RELATED LINKS</span></span>

