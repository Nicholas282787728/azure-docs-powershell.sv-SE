---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: 84a101a427fc5541d4888a0b4deb4c5e3880b1d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577028"
---
# <span data-ttu-id="9f4f9-101">Set-AzureRmEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="9f4f9-101">Set-AzureRmEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="9f4f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9f4f9-102">SYNOPSIS</span></span>
<span data-ttu-id="9f4f9-103">Anropar GEO-failover och konfigurerar om aliaset så att det pekar på det sekundära namn området</span><span class="sxs-lookup"><span data-stu-id="9f4f9-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f4f9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9f4f9-104">SYNTAX</span></span>

### <span data-ttu-id="9f4f9-105">GeoDRParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9f4f9-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9f4f9-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9f4f9-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f4f9-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f4f9-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f4f9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9f4f9-108">DESCRIPTION</span></span>
<span data-ttu-id="9f4f9-109">Cmdleten **set-AzureRmEventHubGeoDRConfigurationFailOver** -ENVOKES geo Dr och konfigurera om aliaset så att det pekar på det sekundära namn området</span><span class="sxs-lookup"><span data-stu-id="9f4f9-109">The **Set-AzureRmEventHubGeoDRConfigurationFailOver** cmdlet envokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="9f4f9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9f4f9-110">EXAMPLES</span></span>

### <span data-ttu-id="9f4f9-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9f4f9-111">Example 1</span></span>
```
PS C:\>Set-AzureRmEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="9f4f9-112">Anropar redundans över alias "SampleDRCongifName", konfigurerar om och pekar på sekundär namn område "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="9f4f9-112">Invokes the Failover over alias "SampleDRCongifName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="9f4f9-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9f4f9-113">PARAMETERS</span></span>

### <span data-ttu-id="9f4f9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f4f9-114">-DefaultProfile</span></span>
<span data-ttu-id="9f4f9-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9f4f9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f4f9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f4f9-116">-InputObject</span></span>
<span data-ttu-id="9f4f9-117">Eventhub-GeoDR</span><span class="sxs-lookup"><span data-stu-id="9f4f9-117">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f4f9-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="9f4f9-118">-Name</span></span>
<span data-ttu-id="9f4f9-119">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="9f4f9-119">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f4f9-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="9f4f9-120">-Namespace</span></span>
<span data-ttu-id="9f4f9-121">Namn områdes namn-sekundärt namn område</span><span class="sxs-lookup"><span data-stu-id="9f4f9-121">Namespace Name - Secondary Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f4f9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f4f9-122">-PassThru</span></span>
<span data-ttu-id="9f4f9-123">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="9f4f9-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9f4f9-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="9f4f9-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9f4f9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f4f9-125">-ResourceGroupName</span></span>
<span data-ttu-id="9f4f9-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="9f4f9-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f4f9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f4f9-127">-ResourceId</span></span>
<span data-ttu-id="9f4f9-128">Resurs-ID för GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="9f4f9-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="9f4f9-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9f4f9-129">-Confirm</span></span>
<span data-ttu-id="9f4f9-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9f4f9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f4f9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f4f9-131">-WhatIf</span></span>
<span data-ttu-id="9f4f9-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9f4f9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f4f9-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9f4f9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f4f9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f4f9-134">CommonParameters</span></span>
<span data-ttu-id="9f4f9-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f4f9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f4f9-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f4f9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f4f9-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9f4f9-137">INPUTS</span></span>

### <span data-ttu-id="9f4f9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9f4f9-138">System.String</span></span>

### <span data-ttu-id="9f4f9-139">Microsoft. Azure. commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="9f4f9-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>
<span data-ttu-id="9f4f9-140">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9f4f9-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="9f4f9-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9f4f9-141">OUTPUTS</span></span>

### <span data-ttu-id="9f4f9-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9f4f9-142">System.Boolean</span></span>

## <span data-ttu-id="9f4f9-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9f4f9-143">NOTES</span></span>

## <span data-ttu-id="9f4f9-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9f4f9-144">RELATED LINKS</span></span>
