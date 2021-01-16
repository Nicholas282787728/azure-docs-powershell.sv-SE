---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppTrafficRouting.md
ms.openlocfilehash: 7fba74a3778df0c8c26ed4b581e5d2777ff75029
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522038"
---
# <span data-ttu-id="3e813-101">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3e813-101">Update-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="3e813-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e813-102">SYNOPSIS</span></span>
<span data-ttu-id="3e813-103">Uppdatera en routningsregler till platsen.</span><span class="sxs-lookup"><span data-stu-id="3e813-103">Update a routing Rule to the Slot.</span></span>

## <span data-ttu-id="3e813-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e813-104">SYNTAX</span></span>

```
Update-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e813-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e813-105">DESCRIPTION</span></span>
<span data-ttu-id="3e813-106">Cmdleten **Update-AzWebAppTrafficRouting** uppdaterar routningstabellen för en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="3e813-106">The **Update-AzWebAppTrafficRouting** cmdlet updates the routing rule configuration for an Azure Web App Slot.</span></span>

## <span data-ttu-id="3e813-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e813-107">EXAMPLES</span></span>

### <span data-ttu-id="3e813-108">Exempel 1 uppdatera en routningsregler för att överföra 15% av produktions trafiken till STG-platsen</span><span class="sxs-lookup"><span data-stu-id="3e813-108">Example 1 Update a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
- RoutingRule @{AtionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="3e813-109">Det här kommandot uppdaterar en routningsregler för överföring av 15% av produktions trafiken till STG-facket.</span><span class="sxs-lookup"><span data-stu-id="3e813-109">This command updates a routing rule to transfer 15% of production traffic to Stg slot.</span></span>

### <span data-ttu-id="3e813-110">Exempel 2 uppdatera en routningsregler för att överföra produktions trafiken till STG-kortplatserna från 50% till 90% på inkrementellt sätt.</span><span class="sxs-lookup"><span data-stu-id="3e813-110">Example 2 Update a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Update-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="3e813-111">Det här kommandot uppdaterar en routningsregler för att överföra produktions trafiken till STG-kortplatserna från 50% till 90% på inkrementellt sätt.</span><span class="sxs-lookup"><span data-stu-id="3e813-111">This command Updates a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="3e813-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e813-112">PARAMETERS</span></span>

### <span data-ttu-id="3e813-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e813-113">-DefaultProfile</span></span>
<span data-ttu-id="3e813-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3e813-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e813-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e813-115">-ResourceGroupName</span></span>
<span data-ttu-id="3e813-116">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e813-116">ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e813-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="3e813-117">-RoutingRule</span></span>
<span data-ttu-id="3e813-118">Web App-RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="3e813-118">Web App RoutingRule.</span></span>
<span data-ttu-id="3e813-119">Exempel:-RoutingRule @ {ActionHostName = $slot. DefaultHostName ; ReroutePercentage = $ReroutePercentage; Namn = $slotName}</span><span class="sxs-lookup"><span data-stu-id="3e813-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e813-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="3e813-120">-WebAppName</span></span>
<span data-ttu-id="3e813-121">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="3e813-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e813-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3e813-122">-Confirm</span></span>
<span data-ttu-id="3e813-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3e813-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e813-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e813-124">-WhatIf</span></span>
<span data-ttu-id="3e813-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3e813-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e813-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3e813-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e813-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e813-127">CommonParameters</span></span>
<span data-ttu-id="3e813-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e813-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e813-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e813-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e813-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e813-130">INPUTS</span></span>

### <span data-ttu-id="3e813-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="3e813-131">None</span></span>

## <span data-ttu-id="3e813-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e813-132">OUTPUTS</span></span>

### <span data-ttu-id="3e813-133">Microsoft. Azure. Management. webbplatser. Models. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="3e813-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="3e813-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e813-134">NOTES</span></span>

## <span data-ttu-id="3e813-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e813-135">RELATED LINKS</span></span>

[<span data-ttu-id="3e813-136">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3e813-136">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="3e813-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3e813-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="3e813-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3e813-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)