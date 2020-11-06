---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
ms.openlocfilehash: a28fe30424b5b1d29c3b671e5cec266fc75d9dbb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582588"
---
# <span data-ttu-id="aa68e-101">New-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="aa68e-101">New-AzureRmRouteFilter</span></span>

## <span data-ttu-id="aa68e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aa68e-102">SYNOPSIS</span></span>
<span data-ttu-id="aa68e-103">Skapar ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="aa68e-103">Creates a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa68e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aa68e-104">SYNTAX</span></span>

```
New-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa68e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aa68e-105">DESCRIPTION</span></span>
<span data-ttu-id="aa68e-106">New-AzureRmRouteFilter-cmdleten skapar ett Azure Route-filter.</span><span class="sxs-lookup"><span data-stu-id="aa68e-106">The New-AzureRmRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="aa68e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aa68e-107">EXAMPLES</span></span>

### <span data-ttu-id="aa68e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="aa68e-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="aa68e-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="aa68e-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="aa68e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aa68e-110">PARAMETERS</span></span>

### <span data-ttu-id="aa68e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa68e-111">-AsJob</span></span>
<span data-ttu-id="aa68e-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="aa68e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa68e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa68e-113">-DefaultProfile</span></span>
<span data-ttu-id="aa68e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="aa68e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa68e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="aa68e-115">-Force</span></span>
<span data-ttu-id="aa68e-116">Anger att den här cmdleten skapar en routningstabell även om ett väg filter med samma namn redan finns.</span><span class="sxs-lookup"><span data-stu-id="aa68e-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="aa68e-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="aa68e-117">-Location</span></span>
<span data-ttu-id="aa68e-118">Anger det Azure-område där den här cmdleten skapar ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="aa68e-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="aa68e-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="aa68e-119">-Name</span></span>
<span data-ttu-id="aa68e-120">Anger ett namn för väg filtret.</span><span class="sxs-lookup"><span data-stu-id="aa68e-120">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="aa68e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa68e-121">-ResourceGroupName</span></span>
<span data-ttu-id="aa68e-122">Anger namnet på resurs gruppen där denna cmdlet skapar ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="aa68e-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="aa68e-123">-Regel</span><span class="sxs-lookup"><span data-stu-id="aa68e-123">-Rule</span></span>
<span data-ttu-id="aa68e-124">Anger en matris med rutt filter regel objekt som ska kopplas till väg filtret.</span><span class="sxs-lookup"><span data-stu-id="aa68e-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa68e-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="aa68e-125">-Tag</span></span>
<span data-ttu-id="aa68e-126">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="aa68e-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="aa68e-127">Till exempel: @ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="aa68e-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="aa68e-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="aa68e-128">-Confirm</span></span>
<span data-ttu-id="aa68e-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="aa68e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa68e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa68e-130">-WhatIf</span></span>
<span data-ttu-id="aa68e-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="aa68e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa68e-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="aa68e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa68e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa68e-133">CommonParameters</span></span>
<span data-ttu-id="aa68e-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa68e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa68e-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa68e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa68e-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aa68e-136">INPUTS</span></span>

### <span data-ttu-id="aa68e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="aa68e-137">System.String</span></span>

### <span data-ttu-id="aa68e-138">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSRouteFilterRule, Microsoft. Azure. commands. Network, version = 6.4.1.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="aa68e-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="aa68e-139">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="aa68e-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="aa68e-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aa68e-140">OUTPUTS</span></span>

### <span data-ttu-id="aa68e-141">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="aa68e-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="aa68e-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aa68e-142">NOTES</span></span>
<span data-ttu-id="aa68e-143">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="aa68e-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="aa68e-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aa68e-144">RELATED LINKS</span></span>

[<span data-ttu-id="aa68e-145">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="aa68e-145">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="aa68e-146">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="aa68e-146">New-AzureRmRouteFilterRuleConfig</span></span>](./New-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="aa68e-147">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="aa68e-147">Remove-AzureRmRouteFilter</span></span>](./Remove-AzureRmRouteFilter.md)

[<span data-ttu-id="aa68e-148">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="aa68e-148">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)
