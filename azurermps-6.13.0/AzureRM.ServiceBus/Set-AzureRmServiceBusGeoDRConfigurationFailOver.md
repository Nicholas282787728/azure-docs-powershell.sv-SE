---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusGeoDRConfigurationFailOver.md
ms.openlocfilehash: 274563165beefdc8a5d7575bd32328f68bf40efa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582551"
---
# <span data-ttu-id="815ba-101">Set-AzureRmServiceBusGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="815ba-101">Set-AzureRmServiceBusGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="815ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="815ba-102">SYNOPSIS</span></span>
<span data-ttu-id="815ba-103">Anropar GEO-failover och konfigurerar om aliaset så att det pekar på det sekundära namn området</span><span class="sxs-lookup"><span data-stu-id="815ba-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="815ba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="815ba-104">SYNTAX</span></span>

### <span data-ttu-id="815ba-105">GeoDRPropertiesSet (standard)</span><span class="sxs-lookup"><span data-stu-id="815ba-105">GeoDRPropertiesSet (Default)</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="815ba-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="815ba-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-InputObject] <PSServiceBusDRConfigurationAttributes>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="815ba-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="815ba-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmServiceBusGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="815ba-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="815ba-108">DESCRIPTION</span></span>
<span data-ttu-id="815ba-109">Cmdleten **set-AzureRmServiceBusGeoDRConfigurationFailOver** -ENVOKES geo Dr och konfigurera om aliaset så att det pekar på det sekundära namn området</span><span class="sxs-lookup"><span data-stu-id="815ba-109">The **Set-AzureRmServiceBusGeoDRConfigurationFailOver** cmdlet envokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="815ba-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="815ba-110">EXAMPLES</span></span>

### <span data-ttu-id="815ba-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="815ba-111">Example 1</span></span>
```
PS C:\> Set-AzureRmServiceBusGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="815ba-112">Anropar redundans över alias "SampleDRCongifName", konfigurerar om och pekar på sekundär namn område "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="815ba-112">Invokes the Failover over alias "SampleDRCongifName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="815ba-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="815ba-113">PARAMETERS</span></span>

### <span data-ttu-id="815ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="815ba-114">-DefaultProfile</span></span>
<span data-ttu-id="815ba-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="815ba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="815ba-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="815ba-116">-InputObject</span></span>
<span data-ttu-id="815ba-117">Service Bus GeoDR konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="815ba-117">Service Bus GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="815ba-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="815ba-118">-Name</span></span>
<span data-ttu-id="815ba-119">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="815ba-119">DR Configuration Name - Alias</span></span>

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

### <span data-ttu-id="815ba-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="815ba-120">-Namespace</span></span>
<span data-ttu-id="815ba-121">Namn områdes namn-sekundärt namn område</span><span class="sxs-lookup"><span data-stu-id="815ba-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="815ba-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="815ba-122">-PassThru</span></span>
<span data-ttu-id="815ba-123">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="815ba-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="815ba-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="815ba-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="815ba-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="815ba-125">-ResourceGroupName</span></span>
<span data-ttu-id="815ba-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="815ba-126">Resource Group Name</span></span>

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

### <span data-ttu-id="815ba-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="815ba-127">-ResourceId</span></span>
<span data-ttu-id="815ba-128">Resurs-ID för GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="815ba-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="815ba-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="815ba-129">-Confirm</span></span>
<span data-ttu-id="815ba-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="815ba-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="815ba-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="815ba-131">-WhatIf</span></span>
<span data-ttu-id="815ba-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="815ba-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="815ba-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="815ba-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="815ba-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="815ba-134">CommonParameters</span></span>
<span data-ttu-id="815ba-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="815ba-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="815ba-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="815ba-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="815ba-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="815ba-137">INPUTS</span></span>

### <span data-ttu-id="815ba-138">System. String</span><span class="sxs-lookup"><span data-stu-id="815ba-138">System.String</span></span>

### <span data-ttu-id="815ba-139">Microsoft. Azure. commands. ServiceBus. Models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="815ba-139">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="815ba-140">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="815ba-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="815ba-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="815ba-141">OUTPUTS</span></span>

### <span data-ttu-id="815ba-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="815ba-142">System.Boolean</span></span>

## <span data-ttu-id="815ba-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="815ba-143">NOTES</span></span>

## <span data-ttu-id="815ba-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="815ba-144">RELATED LINKS</span></span>
