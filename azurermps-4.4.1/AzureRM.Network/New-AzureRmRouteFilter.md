---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
ms.openlocfilehash: 6cc420ccb2ba2c7e555956d711fe0e30d02ef62f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575989"
---
# <span data-ttu-id="0a043-101">New-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0a043-101">New-AzureRmRouteFilter</span></span>

## <span data-ttu-id="0a043-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0a043-102">SYNOPSIS</span></span>
<span data-ttu-id="0a043-103">Skapar ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="0a043-103">Creates a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a043-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0a043-104">SYNTAX</span></span>

```
New-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a043-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0a043-105">DESCRIPTION</span></span>
<span data-ttu-id="0a043-106">New-AzureRmRouteFilter-cmdleten skapar ett Azure Route-filter.</span><span class="sxs-lookup"><span data-stu-id="0a043-106">The New-AzureRmRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="0a043-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0a043-107">EXAMPLES</span></span>

### <span data-ttu-id="0a043-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0a043-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="0a043-109">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="0a043-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="0a043-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0a043-110">PARAMETERS</span></span>

### <span data-ttu-id="0a043-111">-Force</span><span class="sxs-lookup"><span data-stu-id="0a043-111">-Force</span></span>
<span data-ttu-id="0a043-112">Anger att den här cmdleten skapar en routningstabell även om ett väg filter med samma namn redan finns.</span><span class="sxs-lookup"><span data-stu-id="0a043-112">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="0a043-113">-Plats</span><span class="sxs-lookup"><span data-stu-id="0a043-113">-Location</span></span>
<span data-ttu-id="0a043-114">Anger det Azure-område där den här cmdleten skapar ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="0a043-114">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="0a043-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="0a043-115">-Name</span></span>
<span data-ttu-id="0a043-116">Anger ett namn för väg filtret.</span><span class="sxs-lookup"><span data-stu-id="0a043-116">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="0a043-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a043-117">-ResourceGroupName</span></span>
<span data-ttu-id="0a043-118">Anger namnet på resurs gruppen där denna cmdlet skapar ett väg filter.</span><span class="sxs-lookup"><span data-stu-id="0a043-118">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="0a043-119">-Regel</span><span class="sxs-lookup"><span data-stu-id="0a043-119">-Rule</span></span>
<span data-ttu-id="0a043-120">Anger en matris med rutt filter regel objekt som ska kopplas till väg filtret.</span><span class="sxs-lookup"><span data-stu-id="0a043-120">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="0a043-121">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0a043-121">-Tag</span></span>
<span data-ttu-id="0a043-122">Par med nyckelord i form av en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="0a043-122">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0a043-123">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="0a043-123">For example:</span></span>

<span data-ttu-id="0a043-124">@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}</span><span class="sxs-lookup"><span data-stu-id="0a043-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0a043-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0a043-125">-Confirm</span></span>
<span data-ttu-id="0a043-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0a043-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a043-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a043-127">-WhatIf</span></span>
<span data-ttu-id="0a043-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0a043-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a043-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0a043-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a043-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a043-130">-DefaultProfile</span></span>
<span data-ttu-id="0a043-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0a043-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a043-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a043-132">CommonParameters</span></span>
<span data-ttu-id="0a043-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a043-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a043-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a043-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a043-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0a043-135">INPUTS</span></span>

## <span data-ttu-id="0a043-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0a043-136">OUTPUTS</span></span>

### <span data-ttu-id="0a043-137">Microsoft. Azure. commands. Networks. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0a043-137">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="0a043-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0a043-138">NOTES</span></span>
<span data-ttu-id="0a043-139">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk</span><span class="sxs-lookup"><span data-stu-id="0a043-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="0a043-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0a043-140">RELATED LINKS</span></span>

[<span data-ttu-id="0a043-141">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0a043-141">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="0a043-142">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a043-142">New-AzureRmRouteFilterRuleConfig</span></span>](./New-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="0a043-143">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0a043-143">Remove-AzureRmRouteFilter</span></span>](./Remove-AzureRmRouteFilter.md)

[<span data-ttu-id="0a043-144">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="0a043-144">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)
