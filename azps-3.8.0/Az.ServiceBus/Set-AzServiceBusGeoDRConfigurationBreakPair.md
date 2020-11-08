---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationBreakPair.md
ms.openlocfilehash: f45899b1c2d397245461a10a6e2648f92dc9da40
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088820"
---
# <span data-ttu-id="9f0be-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="9f0be-101">Set-AzServiceBusGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="9f0be-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9f0be-102">SYNOPSIS</span></span>
<span data-ttu-id="9f0be-103">Den här åtgärden inaktiverar katastrof återställning och upphör att replikera ändringar från primära till sekundära namn områden</span><span class="sxs-lookup"><span data-stu-id="9f0be-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="9f0be-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9f0be-104">SYNTAX</span></span>

### <span data-ttu-id="9f0be-105">GeoDRPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9f0be-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9f0be-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9f0be-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f0be-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f0be-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f0be-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9f0be-108">DESCRIPTION</span></span>
<span data-ttu-id="9f0be-109">Cmdleten **set-AzServiceBusGeoDRConfigurationBreakPair** inaktiverar katastrof återställning och slutar replikera ändringar från primära till sekundära namn områden</span><span class="sxs-lookup"><span data-stu-id="9f0be-109">The **Set-AzServiceBusGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="9f0be-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9f0be-110">EXAMPLES</span></span>

### <span data-ttu-id="9f0be-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9f0be-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="9f0be-112">Den här åtgärden inaktiverar katastrof återställning och upphör att replikera ändringar från primära till sekundära namn områden</span><span class="sxs-lookup"><span data-stu-id="9f0be-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="9f0be-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9f0be-113">PARAMETERS</span></span>

### <span data-ttu-id="9f0be-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f0be-114">-DefaultProfile</span></span>
<span data-ttu-id="9f0be-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9f0be-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f0be-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f0be-116">-InputObject</span></span>
<span data-ttu-id="9f0be-117">Service Bus GeoDR konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="9f0be-117">Service Bus GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f0be-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="9f0be-118">-Name</span></span>
<span data-ttu-id="9f0be-119">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="9f0be-119">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f0be-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="9f0be-120">-Namespace</span></span>
<span data-ttu-id="9f0be-121">Namn områdes namn – primär namnrymd</span><span class="sxs-lookup"><span data-stu-id="9f0be-121">Namespace Name - Primary Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f0be-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f0be-122">-PassThru</span></span>
<span data-ttu-id="9f0be-123">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="9f0be-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9f0be-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="9f0be-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9f0be-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f0be-125">-ResourceGroupName</span></span>
<span data-ttu-id="9f0be-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="9f0be-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f0be-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f0be-127">-ResourceId</span></span>
<span data-ttu-id="9f0be-128">Resurs-ID för GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f0be-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f0be-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9f0be-129">-Confirm</span></span>
<span data-ttu-id="9f0be-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9f0be-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f0be-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f0be-131">-WhatIf</span></span>
<span data-ttu-id="9f0be-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9f0be-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f0be-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9f0be-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f0be-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f0be-134">CommonParameters</span></span>
<span data-ttu-id="9f0be-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f0be-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f0be-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f0be-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f0be-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9f0be-137">INPUTS</span></span>

### <span data-ttu-id="9f0be-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9f0be-138">System.String</span></span>

### <span data-ttu-id="9f0be-139">Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="9f0be-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="9f0be-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9f0be-140">OUTPUTS</span></span>

### <span data-ttu-id="9f0be-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9f0be-141">System.Boolean</span></span>

## <span data-ttu-id="9f0be-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9f0be-142">NOTES</span></span>

## <span data-ttu-id="9f0be-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9f0be-143">RELATED LINKS</span></span>
