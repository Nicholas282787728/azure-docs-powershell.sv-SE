---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: 3ee0e251f4dd92b087343edc03e829e8032ee5c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577030"
---
# <span data-ttu-id="ef1d0-101">Set-AzureRmEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="ef1d0-101">Set-AzureRmEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="ef1d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef1d0-102">SYNOPSIS</span></span>
<span data-ttu-id="ef1d0-103">Den här åtgärden inaktiverar katastrof återställning och upphör att replikera ändringar från primära till sekundära namn områden</span><span class="sxs-lookup"><span data-stu-id="ef1d0-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef1d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef1d0-104">SYNTAX</span></span>

### <span data-ttu-id="ef1d0-105">GeoDRParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ef1d0-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef1d0-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ef1d0-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef1d0-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef1d0-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef1d0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef1d0-108">DESCRIPTION</span></span>
<span data-ttu-id="ef1d0-109">Cmdleten **set-AzureRmEventHubGeoDRConfigurationBreakPair** inaktiverar katastrof återställning och slutar replikera ändringar från primära till sekundära namn områden</span><span class="sxs-lookup"><span data-stu-id="ef1d0-109">The **Set-AzureRmEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="ef1d0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef1d0-110">EXAMPLES</span></span>

### <span data-ttu-id="ef1d0-111">Exempel</span><span class="sxs-lookup"><span data-stu-id="ef1d0-111">Example</span></span>
```
PS C:\> Set-AzureRmEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"
```

<span data-ttu-id="ef1d0-112">Den här åtgärden inaktiverar katastrof återställning och upphör att replikera ändringar från primära till sekundära namn områden</span><span class="sxs-lookup"><span data-stu-id="ef1d0-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="ef1d0-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef1d0-113">PARAMETERS</span></span>

### <span data-ttu-id="ef1d0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef1d0-114">-DefaultProfile</span></span>
<span data-ttu-id="ef1d0-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ef1d0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef1d0-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef1d0-116">-InputObject</span></span>
<span data-ttu-id="ef1d0-117">Eventhub-GeoDR</span><span class="sxs-lookup"><span data-stu-id="ef1d0-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="ef1d0-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ef1d0-118">-Name</span></span>
<span data-ttu-id="ef1d0-119">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="ef1d0-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="ef1d0-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="ef1d0-120">-Namespace</span></span>
<span data-ttu-id="ef1d0-121">Namn områdes namn – primär namnrymd</span><span class="sxs-lookup"><span data-stu-id="ef1d0-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="ef1d0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef1d0-122">-PassThru</span></span>
<span data-ttu-id="ef1d0-123">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="ef1d0-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ef1d0-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="ef1d0-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ef1d0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef1d0-125">-ResourceGroupName</span></span>
<span data-ttu-id="ef1d0-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="ef1d0-126">Resource Group Name</span></span>

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

### <span data-ttu-id="ef1d0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef1d0-127">-ResourceId</span></span>
<span data-ttu-id="ef1d0-128">Resurs-ID för GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef1d0-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="ef1d0-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ef1d0-129">-Confirm</span></span>
<span data-ttu-id="ef1d0-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ef1d0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef1d0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef1d0-131">-WhatIf</span></span>
<span data-ttu-id="ef1d0-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ef1d0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef1d0-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ef1d0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef1d0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef1d0-134">CommonParameters</span></span>
<span data-ttu-id="ef1d0-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef1d0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef1d0-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef1d0-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef1d0-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef1d0-137">INPUTS</span></span>

### <span data-ttu-id="ef1d0-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ef1d0-138">System.String</span></span>

### <span data-ttu-id="ef1d0-139">Microsoft. Azure. commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="ef1d0-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>
<span data-ttu-id="ef1d0-140">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ef1d0-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ef1d0-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef1d0-141">OUTPUTS</span></span>

### <span data-ttu-id="ef1d0-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ef1d0-142">System.Boolean</span></span>

## <span data-ttu-id="ef1d0-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef1d0-143">NOTES</span></span>

## <span data-ttu-id="ef1d0-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef1d0-144">RELATED LINKS</span></span>
