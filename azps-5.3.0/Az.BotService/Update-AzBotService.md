---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/update-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
ms.openlocfilehash: f7dd02a214fa32223e052c1999329699f1c653e9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527168"
---
# <span data-ttu-id="c7d3d-101">Update-AzBotService</span><span class="sxs-lookup"><span data-stu-id="c7d3d-101">Update-AzBotService</span></span>

## <span data-ttu-id="c7d3d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c7d3d-102">SYNOPSIS</span></span>
<span data-ttu-id="c7d3d-103">Uppdaterar en robot tjänst</span><span class="sxs-lookup"><span data-stu-id="c7d3d-103">Updates a Bot Service</span></span>

## <span data-ttu-id="c7d3d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c7d3d-104">SYNTAX</span></span>

### <span data-ttu-id="c7d3d-105">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="c7d3d-105">UpdateExpanded (Default)</span></span>
```
Update-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c7d3d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c7d3d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBotService -InputObject <IBotServiceIdentity> [-Description <String>]
 [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c7d3d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c7d3d-107">DESCRIPTION</span></span>
<span data-ttu-id="c7d3d-108">Uppdaterar en robot tjänst</span><span class="sxs-lookup"><span data-stu-id="c7d3d-108">Updates a Bot Service</span></span>

## <span data-ttu-id="c7d3d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c7d3d-109">EXAMPLES</span></span>

### <span data-ttu-id="c7d3d-110">Exempel 1: uppdatera roboten med namn och ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7d3d-110">Example 1: Update the Bot by Name and ResourceGroupName</span></span>
```powershell
PS C:\> Update-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest' -kind Bot

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"0700e71b-0000-1800-0000-5fd73ed80000" Bot  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="c7d3d-111">Uppdatera roboten med namn och ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7d3d-111">Update the Bot by Name and ResourceGroupName</span></span>

### <span data-ttu-id="c7d3d-112">Exempel 2: uppdatera roboten med InputObject</span><span class="sxs-lookup"><span data-stu-id="c7d3d-112">Example 2: Update the Bot by InputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest'
Update-AzBotService -InputObject $getAzbot -kind sdk

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"07008b1c-0000-1800-0000-5fd73f9e0000" sdk  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="c7d3d-113">Uppdatera roboten med InputObject</span><span class="sxs-lookup"><span data-stu-id="c7d3d-113">Update the Bot by InputObject</span></span>

## <span data-ttu-id="c7d3d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c7d3d-114">PARAMETERS</span></span>

### <span data-ttu-id="c7d3d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7d3d-115">-DefaultProfile</span></span>
<span data-ttu-id="c7d3d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d3d-117">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="c7d3d-117">-Description</span></span>
<span data-ttu-id="c7d3d-118">Beskrivningen av bot</span><span class="sxs-lookup"><span data-stu-id="c7d3d-118">The description of the bot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d3d-119">-DeveloperAppInsightKey</span><span class="sxs-lookup"><span data-stu-id="c7d3d-119">-DeveloperAppInsightKey</span></span>
<span data-ttu-id="c7d3d-120">Knappen Application Insights</span><span class="sxs-lookup"><span data-stu-id="c7d3d-120">The Application Insights key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d3d-121">-DeveloperAppInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="c7d3d-121">-DeveloperAppInsightsApiKey</span></span>
<span data-ttu-id="c7d3d-122">API-tangenten för Application Insights</span><span class="sxs-lookup"><span data-stu-id="c7d3d-122">The Application Insights Api Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d3d-123">-DeveloperAppInsightsApplicationId</span><span class="sxs-lookup"><span data-stu-id="c7d3d-123">-DeveloperAppInsightsApplicationId</span></span>
<span data-ttu-id="c7d3d-124">App-ID för Application Insights</span><span class="sxs-lookup"><span data-stu-id="c7d3d-124">The Application Insights App Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d3d-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c7d3d-125">-DisplayName</span></span>
<span data-ttu-id="c7d3d-126">Namnet på roboten</span><span class="sxs-lookup"><span data-stu-id="c7d3d-126">The Name of the bot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d3d-127">-Slut punkt</span><span class="sxs-lookup"><span data-stu-id="c7d3d-127">-Endpoint</span></span>
<span data-ttu-id="c7d3d-128">Robotens slut punkt</span><span class="sxs-lookup"><span data-stu-id="c7d3d-128">The bot's endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d3d-129">-Etag</span><span class="sxs-lookup"><span data-stu-id="c7d3d-129">-Etag</span></span>
<span data-ttu-id="c7d3d-130">Entity-tagg</span><span class="sxs-lookup"><span data-stu-id="c7d3d-130">Entity Tag</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d3d-131">-IconUrl</span><span class="sxs-lookup"><span data-stu-id="c7d3d-131">-IconUrl</span></span>
<span data-ttu-id="c7d3d-132">Ikon-URL: en för bot</span><span class="sxs-lookup"><span data-stu-id="c7d3d-132">The Icon Url of the bot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d3d-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7d3d-133">-InputObject</span></span>
<span data-ttu-id="c7d3d-134">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7d3d-135">-Sort</span><span class="sxs-lookup"><span data-stu-id="c7d3d-135">-Kind</span></span>
<span data-ttu-id="c7d3d-136">Kunna.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-136">Required.</span></span>
<span data-ttu-id="c7d3d-137">Hämtar eller anger typen av resurs.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-137">Gets or sets the Kind of the resource.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Support.Kind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d3d-138">-Plats</span><span class="sxs-lookup"><span data-stu-id="c7d3d-138">-Location</span></span>
<span data-ttu-id="c7d3d-139">Anger platsen för resursen.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-139">Specifies the location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d3d-140">-LuisAppId</span><span class="sxs-lookup"><span data-stu-id="c7d3d-140">-LuisAppId</span></span>
<span data-ttu-id="c7d3d-141">Samling med LUIS-program-ID</span><span class="sxs-lookup"><span data-stu-id="c7d3d-141">Collection of LUIS App Ids</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d3d-142">-LuisKey</span><span class="sxs-lookup"><span data-stu-id="c7d3d-142">-LuisKey</span></span>
<span data-ttu-id="c7d3d-143">LUIS-tangenten</span><span class="sxs-lookup"><span data-stu-id="c7d3d-143">The LUIS Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d3d-144">-MsaAppId</span><span class="sxs-lookup"><span data-stu-id="c7d3d-144">-MsaAppId</span></span>
<span data-ttu-id="c7d3d-145">Microsoft app-ID för bot</span><span class="sxs-lookup"><span data-stu-id="c7d3d-145">Microsoft App Id for the bot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d3d-146">-Namn</span><span class="sxs-lookup"><span data-stu-id="c7d3d-146">-Name</span></span>
<span data-ttu-id="c7d3d-147">Namnet på bot-resursen.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-147">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d3d-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7d3d-148">-ResourceGroupName</span></span>
<span data-ttu-id="c7d3d-149">Namnet på robot resurs gruppen i användar abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-149">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d3d-150">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c7d3d-150">-SkuName</span></span>
<span data-ttu-id="c7d3d-151">SKU-namnet</span><span class="sxs-lookup"><span data-stu-id="c7d3d-151">The sku name</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d3d-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c7d3d-152">-SubscriptionId</span></span>
<span data-ttu-id="c7d3d-153">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-153">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d3d-154">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c7d3d-154">-Tag</span></span>
<span data-ttu-id="c7d3d-155">Innehåller resursfiler som definierats som nycklar/värde par.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-155">Contains resource tags defined as key/value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d3d-156">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c7d3d-156">-Confirm</span></span>
<span data-ttu-id="c7d3d-157">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7d3d-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7d3d-158">-WhatIf</span></span>
<span data-ttu-id="c7d3d-159">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7d3d-160">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7d3d-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7d3d-161">CommonParameters</span></span>
<span data-ttu-id="c7d3d-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7d3d-163">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7d3d-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7d3d-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c7d3d-164">INPUTS</span></span>

### <span data-ttu-id="c7d3d-165">Microsoft. Azure. PowerShell. cmdletar. BotService. Models. IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="c7d3d-165">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="c7d3d-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c7d3d-166">OUTPUTS</span></span>

### <span data-ttu-id="c7d3d-167">Microsoft. Azure. PowerShell. cmdletar. BotService. Models. Api20180712. IBot</span><span class="sxs-lookup"><span data-stu-id="c7d3d-167">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="c7d3d-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c7d3d-168">NOTES</span></span>

<span data-ttu-id="c7d3d-169">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c7d3d-169">ALIASES</span></span>

<span data-ttu-id="c7d3d-170">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="c7d3d-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c7d3d-171">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c7d3d-172">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c7d3d-173">INPUTOBJECT <IBotServiceIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="c7d3d-173">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c7d3d-174">`[ChannelName <ChannelName?>]`: Namnet på kanal resursen.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-174">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="c7d3d-175">`[ConnectionName <String>]`: Namnet på resursen för bot tjänstens anslutnings inställning</span><span class="sxs-lookup"><span data-stu-id="c7d3d-175">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="c7d3d-176">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="c7d3d-176">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c7d3d-177">`[ResourceGroupName <String>]`: Namnet på den här resurs gruppen för bot i användar abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-177">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="c7d3d-178">`[ResourceName <String>]`: Namnet på bot-resursen.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-178">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="c7d3d-179">`[SubscriptionId <String>]`: ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="c7d3d-179">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="c7d3d-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c7d3d-180">RELATED LINKS</span></span>

