---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 05a395ce1244130f5f11eb4e0593a1855dc8fb76
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269944"
---
# <span data-ttu-id="e6f23-101">Set-AzServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="e6f23-101">Set-AzServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="e6f23-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e6f23-102">SYNOPSIS</span></span>
<span data-ttu-id="e6f23-103">Anropar GEO-failover och konfigurerar om aliaset så att det pekar på det sekundära namn området</span><span class="sxs-lookup"><span data-stu-id="e6f23-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="e6f23-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e6f23-104">SYNTAX</span></span>

### <span data-ttu-id="e6f23-105">GeoDRPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e6f23-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6f23-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e6f23-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6f23-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6f23-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6f23-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e6f23-108">DESCRIPTION</span></span>
<span data-ttu-id="e6f23-109">Cmdleten **set-AzServiceBusGeoDRConfigurationFailOver** anropar geo Dr och konfigurerar om aliaset så att det pekar på det sekundära namn området</span><span class="sxs-lookup"><span data-stu-id="e6f23-109">The **Set-AzServiceBusGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="e6f23-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e6f23-110">EXAMPLES</span></span>

### <span data-ttu-id="e6f23-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e6f23-111">Example 1</span></span>
```
PS C:\> Set-AzServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="e6f23-112">Anropar redundans över alias "SampleDRConfigName", konfigurerar om och pekar på sekundär namn område "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="e6f23-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="e6f23-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e6f23-113">PARAMETERS</span></span>

### <span data-ttu-id="e6f23-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6f23-114">-DefaultProfile</span></span>
<span data-ttu-id="e6f23-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e6f23-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6f23-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6f23-116">-InputObject</span></span>
<span data-ttu-id="e6f23-117">Service Bus GeoDR konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="e6f23-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="e6f23-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="e6f23-118">-Name</span></span>
<span data-ttu-id="e6f23-119">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="e6f23-119">DR Configuration Name - Alias</span></span>

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

### <span data-ttu-id="e6f23-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="e6f23-120">-Namespace</span></span>
<span data-ttu-id="e6f23-121">Namn områdes namn-sekundärt namn område</span><span class="sxs-lookup"><span data-stu-id="e6f23-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="e6f23-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6f23-122">-PassThru</span></span>
<span data-ttu-id="e6f23-123">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="e6f23-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e6f23-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="e6f23-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e6f23-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6f23-125">-ResourceGroupName</span></span>
<span data-ttu-id="e6f23-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="e6f23-126">Resource Group Name</span></span>

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

### <span data-ttu-id="e6f23-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6f23-127">-ResourceId</span></span>
<span data-ttu-id="e6f23-128">Resurs-ID för GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6f23-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="e6f23-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e6f23-129">-Confirm</span></span>
<span data-ttu-id="e6f23-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e6f23-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6f23-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6f23-131">-WhatIf</span></span>
<span data-ttu-id="e6f23-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e6f23-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6f23-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e6f23-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6f23-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6f23-134">CommonParameters</span></span>
<span data-ttu-id="e6f23-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6f23-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6f23-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6f23-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6f23-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e6f23-137">INPUTS</span></span>

### <span data-ttu-id="e6f23-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e6f23-138">System.String</span></span>

### <span data-ttu-id="e6f23-139">Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="e6f23-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

## <span data-ttu-id="e6f23-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e6f23-140">OUTPUTS</span></span>

### <span data-ttu-id="e6f23-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e6f23-141">System.Boolean</span></span>

## <span data-ttu-id="e6f23-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e6f23-142">NOTES</span></span>

## <span data-ttu-id="e6f23-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e6f23-143">RELATED LINKS</span></span>
