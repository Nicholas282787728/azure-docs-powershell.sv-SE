---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: 0b02c1bfbeee6fa3a628ea6ffacd04c15e96a440
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922099"
---
# <span data-ttu-id="66a8d-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="66a8d-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="66a8d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66a8d-102">SYNOPSIS</span></span>
<span data-ttu-id="66a8d-103">Skapar ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="66a8d-103">Creates a route filter.</span></span>

## <span data-ttu-id="66a8d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66a8d-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66a8d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66a8d-105">DESCRIPTION</span></span>
<span data-ttu-id="66a8d-106">New-AzRouteFilter-cmdleten skapar ett Azure Route-filter.</span><span class="sxs-lookup"><span data-stu-id="66a8d-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="66a8d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66a8d-107">EXAMPLES</span></span>

### <span data-ttu-id="66a8d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="66a8d-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="66a8d-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="66a8d-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="66a8d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66a8d-110">PARAMETERS</span></span>

### <span data-ttu-id="66a8d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="66a8d-111">-AsJob</span></span>
<span data-ttu-id="66a8d-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="66a8d-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a8d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a8d-113">-DefaultProfile</span></span>
<span data-ttu-id="66a8d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="66a8d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a8d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="66a8d-115">-Force</span></span>
<span data-ttu-id="66a8d-116">Anger att den här cmdleten skapar en routningstabell även om ett väg filter med samma namn redan finns.</span><span class="sxs-lookup"><span data-stu-id="66a8d-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a8d-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="66a8d-117">-Location</span></span>
<span data-ttu-id="66a8d-118">Anger det Azure-område där den här cmdleten skapar ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="66a8d-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66a8d-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="66a8d-119">-Name</span></span>
<span data-ttu-id="66a8d-120">Anger ett namn för väg filtret.</span><span class="sxs-lookup"><span data-stu-id="66a8d-120">Specifies a name for the route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66a8d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66a8d-121">-ResourceGroupName</span></span>
<span data-ttu-id="66a8d-122">Anger namnet på resurs gruppen där denna cmdlet skapar ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="66a8d-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66a8d-123">-Regel</span><span class="sxs-lookup"><span data-stu-id="66a8d-123">-Rule</span></span>
<span data-ttu-id="66a8d-124">Anger en matris med rutt filter regel objekt som ska kopplas till väg filtret.</span><span class="sxs-lookup"><span data-stu-id="66a8d-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="66a8d-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="66a8d-125">-Tag</span></span>
<span data-ttu-id="66a8d-126">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="66a8d-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="66a8d-127">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="66a8d-127">For example:</span></span>

<span data-ttu-id="66a8d-128">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="66a8d-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66a8d-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="66a8d-129">-Confirm</span></span>
<span data-ttu-id="66a8d-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="66a8d-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a8d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66a8d-131">-WhatIf</span></span>
<span data-ttu-id="66a8d-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="66a8d-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="66a8d-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="66a8d-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66a8d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a8d-134">CommonParameters</span></span>
<span data-ttu-id="66a8d-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66a8d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a8d-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66a8d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a8d-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66a8d-137">INPUTS</span></span>

## <span data-ttu-id="66a8d-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66a8d-138">OUTPUTS</span></span>

### <span data-ttu-id="66a8d-139">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="66a8d-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="66a8d-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66a8d-140">NOTES</span></span>
<span data-ttu-id="66a8d-141">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="66a8d-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="66a8d-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66a8d-142">RELATED LINKS</span></span>

[<span data-ttu-id="66a8d-143">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="66a8d-143">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="66a8d-144">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="66a8d-144">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="66a8d-145">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="66a8d-145">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="66a8d-146">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="66a8d-146">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
