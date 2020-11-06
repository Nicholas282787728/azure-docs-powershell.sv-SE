---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationBreakPair.md
ms.openlocfilehash: a12f22260ce8ee5412cd17ddfa420a7d23f82008
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576761"
---
# <span data-ttu-id="f5200-101">Set-AzureRmServiceBusGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="f5200-101">Set-AzureRmServiceBusGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="f5200-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f5200-102">SYNOPSIS</span></span>
<span data-ttu-id="f5200-103">Den här åtgärden inaktiverar katastrof återställning och upphör att replikera ändringar från primära till sekundära namn områden</span><span class="sxs-lookup"><span data-stu-id="f5200-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5200-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f5200-104">SYNTAX</span></span>

### <span data-ttu-id="f5200-105">GeoDRPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f5200-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5200-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f5200-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-InputObject] <PSServiceBusDRConfigurationAttributes>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5200-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5200-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5200-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f5200-108">DESCRIPTION</span></span>
<span data-ttu-id="f5200-109">Cmdleten **set-AzureRmServiceBusGeoDRConfigurationBreakPair** inaktiverar katastrof återställning och slutar replikera ändringar från primära till sekundära namn områden</span><span class="sxs-lookup"><span data-stu-id="f5200-109">The **Set-AzureRmServiceBusGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="f5200-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f5200-110">EXAMPLES</span></span>

### <span data-ttu-id="f5200-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f5200-111">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"
```

<span data-ttu-id="f5200-112">Den här åtgärden inaktiverar katastrof återställning och upphör att replikera ändringar från primära till sekundära namn områden</span><span class="sxs-lookup"><span data-stu-id="f5200-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="f5200-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f5200-113">PARAMETERS</span></span>

### <span data-ttu-id="f5200-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5200-114">-DefaultProfile</span></span>
<span data-ttu-id="f5200-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f5200-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5200-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5200-116">-InputObject</span></span>
<span data-ttu-id="f5200-117">Service Bus GeoDR konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="f5200-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="f5200-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="f5200-118">-Name</span></span>
<span data-ttu-id="f5200-119">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="f5200-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="f5200-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="f5200-120">-Namespace</span></span>
<span data-ttu-id="f5200-121">Namn områdes namn – primär namnrymd</span><span class="sxs-lookup"><span data-stu-id="f5200-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="f5200-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5200-122">-PassThru</span></span>
<span data-ttu-id="f5200-123">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="f5200-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f5200-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="f5200-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f5200-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5200-125">-ResourceGroupName</span></span>
<span data-ttu-id="f5200-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="f5200-126">Resource Group Name</span></span>

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

### <span data-ttu-id="f5200-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5200-127">-ResourceId</span></span>
<span data-ttu-id="f5200-128">Resurs-ID för GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5200-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="f5200-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f5200-129">-Confirm</span></span>
<span data-ttu-id="f5200-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f5200-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5200-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5200-131">-WhatIf</span></span>
<span data-ttu-id="f5200-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f5200-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5200-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f5200-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5200-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5200-134">CommonParameters</span></span>
<span data-ttu-id="f5200-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5200-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5200-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5200-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5200-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f5200-137">INPUTS</span></span>

### <span data-ttu-id="f5200-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f5200-138">System.String</span></span>

### <span data-ttu-id="f5200-139">Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="f5200-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="f5200-140">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f5200-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f5200-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f5200-141">OUTPUTS</span></span>

### <span data-ttu-id="f5200-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f5200-142">System.Boolean</span></span>

## <span data-ttu-id="f5200-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f5200-143">NOTES</span></span>

## <span data-ttu-id="f5200-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f5200-144">RELATED LINKS</span></span>
