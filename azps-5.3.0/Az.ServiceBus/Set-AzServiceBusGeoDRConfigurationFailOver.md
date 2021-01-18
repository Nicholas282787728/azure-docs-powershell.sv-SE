---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 05a395ce1244130f5f11eb4e0593a1855dc8fb76
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525477"
---
# <span data-ttu-id="c1fc8-101">Set-AzServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="c1fc8-101">Set-AzServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="c1fc8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c1fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="c1fc8-103">Anropar GEO-failover och konfigurerar om aliaset så att det pekar på det sekundära namn området</span><span class="sxs-lookup"><span data-stu-id="c1fc8-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="c1fc8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c1fc8-104">SYNTAX</span></span>

### <span data-ttu-id="c1fc8-105">GeoDRPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c1fc8-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1fc8-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c1fc8-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1fc8-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1fc8-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1fc8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c1fc8-108">DESCRIPTION</span></span>
<span data-ttu-id="c1fc8-109">Cmdleten **set-AzServiceBusGeoDRConfigurationFailOver** anropar geo Dr och konfigurerar om aliaset så att det pekar på det sekundära namn området</span><span class="sxs-lookup"><span data-stu-id="c1fc8-109">The **Set-AzServiceBusGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="c1fc8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c1fc8-110">EXAMPLES</span></span>

### <span data-ttu-id="c1fc8-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c1fc8-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="c1fc8-112">Anropar redundans över alias "SampleDRConfigName", konfigurerar om och pekar på sekundär namn område "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="c1fc8-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="c1fc8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c1fc8-113">PARAMETERS</span></span>

### <span data-ttu-id="c1fc8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1fc8-114">-DefaultProfile</span></span>
<span data-ttu-id="c1fc8-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c1fc8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1fc8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1fc8-116">-InputObject</span></span>
<span data-ttu-id="c1fc8-117">Service Bus GeoDR konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="c1fc8-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="c1fc8-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="c1fc8-118">-Name</span></span>
<span data-ttu-id="c1fc8-119">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="c1fc8-119">DR Configuration Name - Alias</span></span>

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

### <span data-ttu-id="c1fc8-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="c1fc8-120">-Namespace</span></span>
<span data-ttu-id="c1fc8-121">Namn områdes namn-sekundärt namn område</span><span class="sxs-lookup"><span data-stu-id="c1fc8-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="c1fc8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1fc8-122">-PassThru</span></span>
<span data-ttu-id="c1fc8-123">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="c1fc8-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c1fc8-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="c1fc8-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c1fc8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1fc8-125">-ResourceGroupName</span></span>
<span data-ttu-id="c1fc8-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="c1fc8-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1fc8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1fc8-127">-ResourceId</span></span>
<span data-ttu-id="c1fc8-128">Resurs-ID för GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1fc8-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="c1fc8-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c1fc8-129">-Confirm</span></span>
<span data-ttu-id="c1fc8-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c1fc8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1fc8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1fc8-131">-WhatIf</span></span>
<span data-ttu-id="c1fc8-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c1fc8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1fc8-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c1fc8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1fc8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1fc8-134">CommonParameters</span></span>
<span data-ttu-id="c1fc8-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1fc8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1fc8-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1fc8-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1fc8-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c1fc8-137">INPUTS</span></span>

### <span data-ttu-id="c1fc8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c1fc8-138">System.String</span></span>

### <span data-ttu-id="c1fc8-139">Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="c1fc8-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="c1fc8-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c1fc8-140">OUTPUTS</span></span>

### <span data-ttu-id="c1fc8-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c1fc8-141">System.Boolean</span></span>

## <span data-ttu-id="c1fc8-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c1fc8-142">NOTES</span></span>

## <span data-ttu-id="c1fc8-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c1fc8-143">RELATED LINKS</span></span>
