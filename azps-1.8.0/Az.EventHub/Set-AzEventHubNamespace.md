---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: c75b456021368ea72a72bd0b0fea07a0f13d06dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754039"
---
# <span data-ttu-id="4a22b-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="4a22b-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="4a22b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4a22b-102">SYNOPSIS</span></span>
<span data-ttu-id="4a22b-103">Uppdaterar namn området för de angivna Event Hub.</span><span class="sxs-lookup"><span data-stu-id="4a22b-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="4a22b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4a22b-104">SYNTAX</span></span>

### <span data-ttu-id="4a22b-105">NamespaceParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4a22b-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a22b-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a22b-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a22b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4a22b-107">DESCRIPTION</span></span>
<span data-ttu-id="4a22b-108">Set-AzEventHubNamespace cmdlet uppdaterar egenskaperna för de angivna namn områdena för händelse nav.</span><span class="sxs-lookup"><span data-stu-id="4a22b-108">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="4a22b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4a22b-109">EXAMPLES</span></span>

### <span data-ttu-id="4a22b-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4a22b-110">Example 1</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="4a22b-111">Uppdaterar tillståndet för namespace \` MyNamespaceName \` till skapad.</span><span class="sxs-lookup"><span data-stu-id="4a22b-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="4a22b-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4a22b-112">Example 2</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="4a22b-113">Uppdaterar tillståndet för namn områdes \` MyNamespaceName \` med automittre = Enabled och MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="4a22b-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="4a22b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4a22b-114">PARAMETERS</span></span>

### <span data-ttu-id="4a22b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a22b-115">-DefaultProfile</span></span>
<span data-ttu-id="4a22b-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4a22b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a22b-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="4a22b-117">-EnableAutoInflate</span></span>
<span data-ttu-id="4a22b-118">Anger om autoöka-funktionen är aktive rad</span><span class="sxs-lookup"><span data-stu-id="4a22b-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="4a22b-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="4a22b-119">-Location</span></span>
<span data-ttu-id="4a22b-120">Plats för EventHub-namnrymd.</span><span class="sxs-lookup"><span data-stu-id="4a22b-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="4a22b-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="4a22b-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="4a22b-122">Övre gräns för flödes enheter när automittre är aktiverat ska värdet vara inom 0 till 20 data flödes enheter.</span><span class="sxs-lookup"><span data-stu-id="4a22b-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="4a22b-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="4a22b-123">-Name</span></span>
<span data-ttu-id="4a22b-124">Namn område för EventHub.</span><span class="sxs-lookup"><span data-stu-id="4a22b-124">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="4a22b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a22b-125">-ResourceGroupName</span></span>
<span data-ttu-id="4a22b-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="4a22b-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="4a22b-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="4a22b-127">-SkuCapacity</span></span>
<span data-ttu-id="4a22b-128">Eventhub-dataflöden.</span><span class="sxs-lookup"><span data-stu-id="4a22b-128">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="4a22b-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4a22b-129">-SkuName</span></span>
<span data-ttu-id="4a22b-130">Namn på SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="4a22b-130">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="4a22b-131">-State</span><span class="sxs-lookup"><span data-stu-id="4a22b-131">-State</span></span>
<span data-ttu-id="4a22b-132">Inaktivera/aktivera namn område.</span><span class="sxs-lookup"><span data-stu-id="4a22b-132">Disable/Enable Namespace.</span></span>

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

### <span data-ttu-id="4a22b-133">-Tagg</span><span class="sxs-lookup"><span data-stu-id="4a22b-133">-Tag</span></span>
<span data-ttu-id="4a22b-134">Hashtables som representerar en resurs etikett.</span><span class="sxs-lookup"><span data-stu-id="4a22b-134">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="4a22b-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4a22b-135">-Confirm</span></span>
<span data-ttu-id="4a22b-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4a22b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a22b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a22b-137">-WhatIf</span></span>
<span data-ttu-id="4a22b-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4a22b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a22b-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4a22b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a22b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a22b-140">CommonParameters</span></span>
<span data-ttu-id="4a22b-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a22b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a22b-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a22b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a22b-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4a22b-143">INPUTS</span></span>

### <span data-ttu-id="4a22b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4a22b-144">System.String</span></span>

### <span data-ttu-id="4a22b-145">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4a22b-145">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4a22b-146">System. Nullable ' 1 [[Microsoft. Azure. kommandon. EventHub. Models. NamespaceState, Microsoft. Azure. PowerShell. cmdletar. EventHub, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4a22b-146">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="4a22b-147">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="4a22b-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4a22b-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4a22b-148">OUTPUTS</span></span>

### <span data-ttu-id="4a22b-149">Microsoft. Azure. commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="4a22b-149">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="4a22b-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4a22b-150">NOTES</span></span>

## <span data-ttu-id="4a22b-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4a22b-151">RELATED LINKS</span></span>
