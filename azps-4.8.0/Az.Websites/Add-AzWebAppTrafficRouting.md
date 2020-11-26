---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppTrafficRouting.md
ms.openlocfilehash: 8a3949397b12b54062c5cc68f367187f691fb02d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260176"
---
# <span data-ttu-id="743ba-101">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="743ba-101">Add-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="743ba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="743ba-102">SYNOPSIS</span></span>
<span data-ttu-id="743ba-103">Lägga till en routningsregler på platsen.</span><span class="sxs-lookup"><span data-stu-id="743ba-103">Add a routing Rule to the Slot.</span></span>

## <span data-ttu-id="743ba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="743ba-104">SYNTAX</span></span>

```
Add-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RoutingRule <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="743ba-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="743ba-105">DESCRIPTION</span></span>
<span data-ttu-id="743ba-106">Cmdleten **Add-AzWebAppTrafficRouting** lägger till en Synkroniseringsregel till en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="743ba-106">The **Add-AzWebAppTrafficRouting** cmdlet adds a Routing rule to an Azure Web App Slot.</span></span>

## <span data-ttu-id="743ba-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="743ba-107">EXAMPLES</span></span>

### <span data-ttu-id="743ba-108">Exempel 1 lägga till en routningsregler för att överföra 15% av produktions trafiken till STG-platsen</span><span class="sxs-lookup"><span data-stu-id="743ba-108">Example 1 Add a routing rule to transfer 15% of production traffice to  Stg slot</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=15;Name='Stg'}
```

<span data-ttu-id="743ba-109">Det här kommandot lägger till en routningsregler för överföring av 15% av produktions trafiken till STG-platsen</span><span class="sxs-lookup"><span data-stu-id="743ba-109">This command adds a routing rule to transfer 15% of production traffice to  Stg slot</span></span>

### <span data-ttu-id="743ba-110">Exempel 2 lägga till en routningsregler för att överföra produktions trafiken till STG-kortplatserna från 50% till 90% på inkrementellt sätt.</span><span class="sxs-lookup"><span data-stu-id="743ba-110">Example 2 Add a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>
```powershell
PS C:\>Add-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-RoutingRule @{ActionHostName='XXXX.azurewebsites.net';ReroutePercentage=50;ChangeIntervalInMinutes=1;
MinReroutePercentage=50;MaxReroutePercentage=90;Name='Stg';ChangeStep=10}
```

<span data-ttu-id="743ba-111">Det här kommandot lägger till en routningsregler för att överföra produktions trafiken till STG kort platser från 50% till 90% på inkrementellt sätt.</span><span class="sxs-lookup"><span data-stu-id="743ba-111">This command adds a routing rule to transfer the production traffice to Stg slot ranges from 50% to 90% in incremental manner.</span></span>

## <span data-ttu-id="743ba-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="743ba-112">PARAMETERS</span></span>

### <span data-ttu-id="743ba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="743ba-113">-DefaultProfile</span></span>
<span data-ttu-id="743ba-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="743ba-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="743ba-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="743ba-115">-ResourceGroupName</span></span>
<span data-ttu-id="743ba-116">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="743ba-116">Resource Group Name</span></span>

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

### <span data-ttu-id="743ba-117">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="743ba-117">-RoutingRule</span></span>
<span data-ttu-id="743ba-118">Web App-RoutingRule.</span><span class="sxs-lookup"><span data-stu-id="743ba-118">Web App RoutingRule.</span></span>
<span data-ttu-id="743ba-119">Exempel:-RoutingRule @ {ActionHostName = $slot. DefaultHostName ; ReroutePercentage = $ReroutePercentage; Namn = $slotName}</span><span class="sxs-lookup"><span data-stu-id="743ba-119">Example: -RoutingRule @{ActionHostName=$slot.DefaultHostName ; ReroutePercentage=$ReroutePercentage ; Name=$slotName}</span></span>

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

### <span data-ttu-id="743ba-120">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="743ba-120">-WebAppName</span></span>
<span data-ttu-id="743ba-121">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="743ba-121">WebApp Name</span></span>

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

### <span data-ttu-id="743ba-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="743ba-122">-Confirm</span></span>
<span data-ttu-id="743ba-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="743ba-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="743ba-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="743ba-124">-WhatIf</span></span>
<span data-ttu-id="743ba-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="743ba-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="743ba-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="743ba-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="743ba-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="743ba-127">CommonParameters</span></span>
<span data-ttu-id="743ba-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="743ba-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="743ba-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="743ba-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="743ba-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="743ba-130">INPUTS</span></span>

### <span data-ttu-id="743ba-131">Ingen</span><span class="sxs-lookup"><span data-stu-id="743ba-131">None</span></span>

## <span data-ttu-id="743ba-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="743ba-132">OUTPUTS</span></span>

### <span data-ttu-id="743ba-133">Microsoft. Azure. Management. webbplatser. Models. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="743ba-133">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="743ba-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="743ba-134">NOTES</span></span>

## <span data-ttu-id="743ba-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="743ba-135">RELATED LINKS</span></span>
[<span data-ttu-id="743ba-136">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="743ba-136">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="743ba-137">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="743ba-137">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="743ba-138">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="743ba-138">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)