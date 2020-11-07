---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: b89772c1afe621e456dfb269fe869b6cd3fa8a8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748007"
---
# <span data-ttu-id="6cc97-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6cc97-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="6cc97-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6cc97-102">SYNOPSIS</span></span>
<span data-ttu-id="6cc97-103">Skapar ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="6cc97-103">Creates a route filter.</span></span>

## <span data-ttu-id="6cc97-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6cc97-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String> [-Rule <PSRouteFilterRule[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6cc97-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6cc97-105">DESCRIPTION</span></span>
<span data-ttu-id="6cc97-106">New-AzRouteFilter-cmdleten skapar ett Azure Route-filter.</span><span class="sxs-lookup"><span data-stu-id="6cc97-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="6cc97-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6cc97-107">EXAMPLES</span></span>

### <span data-ttu-id="6cc97-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6cc97-108">Example 1</span></span>
```powershell
PS C:\> New-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup" -Location "West US"
```

<span data-ttu-id="6cc97-109">Kommandot skapar ett nytt väg filter.</span><span class="sxs-lookup"><span data-stu-id="6cc97-109">The command creates a new route filter.</span></span>

## <span data-ttu-id="6cc97-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6cc97-110">PARAMETERS</span></span>

### <span data-ttu-id="6cc97-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6cc97-111">-AsJob</span></span>
<span data-ttu-id="6cc97-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6cc97-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6cc97-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cc97-113">-DefaultProfile</span></span>
<span data-ttu-id="6cc97-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6cc97-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cc97-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6cc97-115">-Force</span></span>
<span data-ttu-id="6cc97-116">Anger att den här cmdleten skapar en routningstabell även om ett väg filter med samma namn redan finns.</span><span class="sxs-lookup"><span data-stu-id="6cc97-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="6cc97-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="6cc97-117">-Location</span></span>
<span data-ttu-id="6cc97-118">Anger det Azure-område där den här cmdleten skapar ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="6cc97-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc97-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="6cc97-119">-Name</span></span>
<span data-ttu-id="6cc97-120">Anger ett namn för väg filtret.</span><span class="sxs-lookup"><span data-stu-id="6cc97-120">Specifies a name for the route filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc97-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cc97-121">-ResourceGroupName</span></span>
<span data-ttu-id="6cc97-122">Anger namnet på resurs gruppen där denna cmdlet skapar ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="6cc97-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc97-123">-Regel</span><span class="sxs-lookup"><span data-stu-id="6cc97-123">-Rule</span></span>
<span data-ttu-id="6cc97-124">Anger en matris med rutt filter regel objekt som ska kopplas till väg filtret.</span><span class="sxs-lookup"><span data-stu-id="6cc97-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc97-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="6cc97-125">-Tag</span></span>
<span data-ttu-id="6cc97-126">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="6cc97-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6cc97-127">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="6cc97-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc97-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6cc97-128">-Confirm</span></span>
<span data-ttu-id="6cc97-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6cc97-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cc97-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cc97-130">-WhatIf</span></span>
<span data-ttu-id="6cc97-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6cc97-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6cc97-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6cc97-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cc97-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cc97-133">CommonParameters</span></span>
<span data-ttu-id="6cc97-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cc97-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cc97-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cc97-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cc97-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6cc97-136">INPUTS</span></span>

### <span data-ttu-id="6cc97-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6cc97-137">System.String</span></span>

### <span data-ttu-id="6cc97-138">Microsoft. Azure. commands. Network. Models. PSRouteFilterRule []</span><span class="sxs-lookup"><span data-stu-id="6cc97-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span></span>

### <span data-ttu-id="6cc97-139">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="6cc97-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6cc97-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6cc97-140">OUTPUTS</span></span>

### <span data-ttu-id="6cc97-141">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6cc97-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="6cc97-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6cc97-142">NOTES</span></span>
<span data-ttu-id="6cc97-143">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="6cc97-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="6cc97-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6cc97-144">RELATED LINKS</span></span>

[<span data-ttu-id="6cc97-145">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6cc97-145">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="6cc97-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6cc97-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="6cc97-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6cc97-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="6cc97-148">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6cc97-148">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6cc97-149">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6cc97-149">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6cc97-150">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6cc97-150">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6cc97-151">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6cc97-151">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="6cc97-152">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="6cc97-152">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
