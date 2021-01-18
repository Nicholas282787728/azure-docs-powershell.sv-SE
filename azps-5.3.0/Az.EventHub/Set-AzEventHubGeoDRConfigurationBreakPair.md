---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: f343b92452a34a746d9ff09d5a519519aeaa7a6c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523669"
---
# <span data-ttu-id="4655f-101">Set-AzEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="4655f-101">Set-AzEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="4655f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4655f-102">SYNOPSIS</span></span>
<span data-ttu-id="4655f-103">Den här åtgärden inaktiverar katastrof återställning och upphör att replikera ändringar från primära till sekundära namn områden</span><span class="sxs-lookup"><span data-stu-id="4655f-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="4655f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4655f-104">SYNTAX</span></span>

### <span data-ttu-id="4655f-105">GeoDRParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="4655f-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4655f-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4655f-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4655f-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4655f-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4655f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4655f-108">DESCRIPTION</span></span>
<span data-ttu-id="4655f-109">Cmdleten **set-AzEventHubGeoDRConfigurationBreakPair** inaktiverar katastrof återställning och slutar replikera ändringar från primära till sekundära namn områden</span><span class="sxs-lookup"><span data-stu-id="4655f-109">The **Set-AzEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="4655f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4655f-110">EXAMPLES</span></span>

### <span data-ttu-id="4655f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4655f-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="4655f-112">Den här åtgärden inaktiverar katastrof återställning och upphör att replikera ändringar från primära till sekundära namn områden</span><span class="sxs-lookup"><span data-stu-id="4655f-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="4655f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4655f-113">PARAMETERS</span></span>

### <span data-ttu-id="4655f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4655f-114">-DefaultProfile</span></span>
<span data-ttu-id="4655f-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4655f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4655f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4655f-116">-InputObject</span></span>
<span data-ttu-id="4655f-117">Eventhub-GeoDR</span><span class="sxs-lookup"><span data-stu-id="4655f-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="4655f-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="4655f-118">-Name</span></span>
<span data-ttu-id="4655f-119">Namn på DR-konfiguration</span><span class="sxs-lookup"><span data-stu-id="4655f-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="4655f-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="4655f-120">-Namespace</span></span>
<span data-ttu-id="4655f-121">Namn områdes namn – primär namnrymd</span><span class="sxs-lookup"><span data-stu-id="4655f-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="4655f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4655f-122">-PassThru</span></span>
<span data-ttu-id="4655f-123">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="4655f-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4655f-124">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="4655f-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4655f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4655f-125">-ResourceGroupName</span></span>
<span data-ttu-id="4655f-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="4655f-126">Resource Group Name</span></span>

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

### <span data-ttu-id="4655f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4655f-127">-ResourceId</span></span>
<span data-ttu-id="4655f-128">Resurs-ID för GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="4655f-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="4655f-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4655f-129">-Confirm</span></span>
<span data-ttu-id="4655f-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4655f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4655f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4655f-131">-WhatIf</span></span>
<span data-ttu-id="4655f-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4655f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4655f-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4655f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4655f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4655f-134">CommonParameters</span></span>
<span data-ttu-id="4655f-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4655f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4655f-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4655f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4655f-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4655f-137">INPUTS</span></span>

### <span data-ttu-id="4655f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4655f-138">System.String</span></span>

### <span data-ttu-id="4655f-139">Microsoft. Azure. commands. EventHub. Models. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="4655f-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="4655f-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4655f-140">OUTPUTS</span></span>

### <span data-ttu-id="4655f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4655f-141">System.Boolean</span></span>

## <span data-ttu-id="4655f-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4655f-142">NOTES</span></span>

## <span data-ttu-id="4655f-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4655f-143">RELATED LINKS</span></span>
