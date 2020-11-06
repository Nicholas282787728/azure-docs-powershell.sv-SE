---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
ms.openlocfilehash: 6fd3f000f7c91f0475cd18802dd6a9d096d35f5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580092"
---
# <span data-ttu-id="440c5-101">Set-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="440c5-101">Set-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="440c5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="440c5-102">SYNOPSIS</span></span>
<span data-ttu-id="440c5-103">Uppdaterar namn området för de angivna Event Hub.</span><span class="sxs-lookup"><span data-stu-id="440c5-103">Updates the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="440c5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="440c5-104">SYNTAX</span></span>

### <span data-ttu-id="440c5-105">NamespaceParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="440c5-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="440c5-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="440c5-106">AutoInflateParameterSet</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="440c5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="440c5-107">DESCRIPTION</span></span>
<span data-ttu-id="440c5-108">Set-AzureRmEventHubNamespace cmdlet uppdaterar egenskaperna för de angivna namn områdena för händelse nav.</span><span class="sxs-lookup"><span data-stu-id="440c5-108">The Set-AzureRmEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="440c5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="440c5-109">EXAMPLES</span></span>

### <span data-ttu-id="440c5-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="440c5-110">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="440c5-111">Uppdaterar tillståndet för namespace \` MyNamespaceName \` till skapad.</span><span class="sxs-lookup"><span data-stu-id="440c5-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="440c5-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="440c5-112">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="440c5-113">Uppdaterar tillståndet för namn områdes \` MyNamespaceName \` med automittre = Enabled och MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="440c5-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="440c5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="440c5-114">PARAMETERS</span></span>

### <span data-ttu-id="440c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="440c5-115">-DefaultProfile</span></span>
<span data-ttu-id="440c5-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="440c5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="440c5-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="440c5-117">-EnableAutoInflate</span></span>
<span data-ttu-id="440c5-118">Anger om autoöka-funktionen är aktive rad</span><span class="sxs-lookup"><span data-stu-id="440c5-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="440c5-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="440c5-119">-Location</span></span>
<span data-ttu-id="440c5-120">Plats för EventHub-namnrymd.</span><span class="sxs-lookup"><span data-stu-id="440c5-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="440c5-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="440c5-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="440c5-122">Övre gräns för flödes enheter när automittre är aktiverat ska värdet vara inom 0 till 20 data flödes enheter.</span><span class="sxs-lookup"><span data-stu-id="440c5-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="440c5-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="440c5-123">-Name</span></span>
<span data-ttu-id="440c5-124">Namn område för EventHub.</span><span class="sxs-lookup"><span data-stu-id="440c5-124">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="440c5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="440c5-125">-ResourceGroupName</span></span>
<span data-ttu-id="440c5-126">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="440c5-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="440c5-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="440c5-127">-SkuCapacity</span></span>
<span data-ttu-id="440c5-128">Eventhub-dataflöden.</span><span class="sxs-lookup"><span data-stu-id="440c5-128">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="440c5-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="440c5-129">-SkuName</span></span>
<span data-ttu-id="440c5-130">Namn på SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="440c5-130">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="440c5-131">-State</span><span class="sxs-lookup"><span data-stu-id="440c5-131">-State</span></span>
<span data-ttu-id="440c5-132">Inaktivera/aktivera namn område.</span><span class="sxs-lookup"><span data-stu-id="440c5-132">Disable/Enable Namespace.</span></span>

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

### <span data-ttu-id="440c5-133">-Tagg</span><span class="sxs-lookup"><span data-stu-id="440c5-133">-Tag</span></span>
<span data-ttu-id="440c5-134">Hashtables som representerar en resurs etikett.</span><span class="sxs-lookup"><span data-stu-id="440c5-134">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="440c5-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="440c5-135">-Confirm</span></span>
<span data-ttu-id="440c5-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="440c5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="440c5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="440c5-137">-WhatIf</span></span>
<span data-ttu-id="440c5-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="440c5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="440c5-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="440c5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="440c5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="440c5-140">CommonParameters</span></span>
<span data-ttu-id="440c5-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="440c5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="440c5-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="440c5-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="440c5-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="440c5-143">INPUTS</span></span>

### <span data-ttu-id="440c5-144">System. String</span><span class="sxs-lookup"><span data-stu-id="440c5-144">System.String</span></span>

### <span data-ttu-id="440c5-145">System. Nullable ' 1 [[system. Int32, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="440c5-145">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="440c5-146">System. Nullable ' 1 [[Microsoft. Azure. commands. EventHub. Models. NamespaceState, Microsoft. Azure. commands. EventHub, version = 0.6.7.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="440c5-146">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.Commands.EventHub, Version=0.6.7.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="440c5-147">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="440c5-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="440c5-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="440c5-148">OUTPUTS</span></span>

### <span data-ttu-id="440c5-149">Microsoft. Azure. commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="440c5-149">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="440c5-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="440c5-150">NOTES</span></span>

## <span data-ttu-id="440c5-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="440c5-151">RELATED LINKS</span></span>
