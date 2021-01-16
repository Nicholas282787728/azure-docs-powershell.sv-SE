---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/restart-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Restart-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Restart-AzFunctionApp.md
ms.openlocfilehash: 408adc74257e1260e97c47b24d91cf437b915a5f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523624"
---
# <span data-ttu-id="56ef9-101">Restart-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="56ef9-101">Restart-AzFunctionApp</span></span>

## <span data-ttu-id="56ef9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="56ef9-102">SYNOPSIS</span></span>
<span data-ttu-id="56ef9-103">Startar om en Function-app.</span><span class="sxs-lookup"><span data-stu-id="56ef9-103">Restarts a function app.</span></span>

## <span data-ttu-id="56ef9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="56ef9-104">SYNTAX</span></span>

### <span data-ttu-id="56ef9-105">RestartByName (standard)</span><span class="sxs-lookup"><span data-stu-id="56ef9-105">RestartByName (Default)</span></span>
```
Restart-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="56ef9-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="56ef9-106">ByObjectInput</span></span>
```
Restart-AzFunctionApp -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="56ef9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="56ef9-107">DESCRIPTION</span></span>
<span data-ttu-id="56ef9-108">Startar om en Function-app.</span><span class="sxs-lookup"><span data-stu-id="56ef9-108">Restarts a function app.</span></span>

## <span data-ttu-id="56ef9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="56ef9-109">EXAMPLES</span></span>

### <span data-ttu-id="56ef9-110">Exempel 1: Hämta ett program för en funktion med namn och starta om det.</span><span class="sxs-lookup"><span data-stu-id="56ef9-110">Example 1: Get a function app by name and restart it.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName | Restart-AzFunctionApp -Force
```

<span data-ttu-id="56ef9-111">Det här kommandot får en programfunktion med namn och startar om det.</span><span class="sxs-lookup"><span data-stu-id="56ef9-111">This command gets a function app by name and restarts it.</span></span>

### <span data-ttu-id="56ef9-112">Exempel 2: starta om ett funktions program efter namn.</span><span class="sxs-lookup"><span data-stu-id="56ef9-112">Example 2: Restart a function app by name.</span></span>
```powershell
PS C:\> Restart-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

<span data-ttu-id="56ef9-113">Det här kommandot startar om en Function-app efter namn.</span><span class="sxs-lookup"><span data-stu-id="56ef9-113">This command restarts a function app by name.</span></span>

## <span data-ttu-id="56ef9-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="56ef9-114">PARAMETERS</span></span>

### <span data-ttu-id="56ef9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56ef9-115">-DefaultProfile</span></span>
<span data-ttu-id="56ef9-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="56ef9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56ef9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="56ef9-117">-Force</span></span>
<span data-ttu-id="56ef9-118">Tvingar cmdleten att starta om programmet utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="56ef9-118">Forces the cmdlet to restart the function app without prompting for confirmation.</span></span>

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

### <span data-ttu-id="56ef9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56ef9-119">-InputObject</span></span>
<span data-ttu-id="56ef9-120">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="56ef9-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56ef9-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="56ef9-121">-Name</span></span>
<span data-ttu-id="56ef9-122">Namnet på funktions programmet.</span><span class="sxs-lookup"><span data-stu-id="56ef9-122">The name of function app.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56ef9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56ef9-123">-PassThru</span></span>
<span data-ttu-id="56ef9-124">Returnerar sant när kommandot fungerar.</span><span class="sxs-lookup"><span data-stu-id="56ef9-124">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="56ef9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56ef9-125">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: RestartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56ef9-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56ef9-126">-SubscriptionId</span></span>
<span data-ttu-id="56ef9-127">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="56ef9-127">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56ef9-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="56ef9-128">-Confirm</span></span>
<span data-ttu-id="56ef9-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="56ef9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56ef9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56ef9-130">-WhatIf</span></span>
<span data-ttu-id="56ef9-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="56ef9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56ef9-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="56ef9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56ef9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56ef9-133">CommonParameters</span></span>
<span data-ttu-id="56ef9-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56ef9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56ef9-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56ef9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56ef9-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="56ef9-136">INPUTS</span></span>

### <span data-ttu-id="56ef9-137">Microsoft. Azure. PowerShell. cmdletar. functions. Models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="56ef9-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="56ef9-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="56ef9-138">OUTPUTS</span></span>

### <span data-ttu-id="56ef9-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="56ef9-139">System.Boolean</span></span>

## <span data-ttu-id="56ef9-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="56ef9-140">NOTES</span></span>

<span data-ttu-id="56ef9-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="56ef9-141">ALIASES</span></span>

<span data-ttu-id="56ef9-142">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="56ef9-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="56ef9-143">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="56ef9-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="56ef9-144">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="56ef9-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="56ef9-145">INPUTOBJECT <ISite> :</span><span class="sxs-lookup"><span data-stu-id="56ef9-145">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="56ef9-146">`Location <String>`: Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="56ef9-146">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="56ef9-147">`CloningInfoSourceWebAppId <String>`: Käll programmets ID för ARM-resurs.</span><span class="sxs-lookup"><span data-stu-id="56ef9-147">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="56ef9-148">App-resurs-ID är/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} för produktions platser och/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} för andra platser.</span><span class="sxs-lookup"><span data-stu-id="56ef9-148">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="56ef9-149">`[Kind <String>]`: Typ av resurs.</span><span class="sxs-lookup"><span data-stu-id="56ef9-149">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="56ef9-150">`[Tag <IResourceTags>]`: Resursfiler.</span><span class="sxs-lookup"><span data-stu-id="56ef9-150">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="56ef9-151">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="56ef9-151">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="56ef9-152">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> så här aktiverar du klient tillhörighet <code>false</code> för att sluta skicka cookie-cookies, som dirigerar klienter i samma session till samma instans.</span><span class="sxs-lookup"><span data-stu-id="56ef9-152">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="56ef9-153">Standard är <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="56ef9-153">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="56ef9-154">`[ClientCertEnabled <Boolean?>]`: <code>true</code> så här aktiverar du klientautentisering för klient certifikat (gemensam TLS-verifikation), annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="56ef9-154">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="56ef9-155">Standard är <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="56ef9-155">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="56ef9-156">`[ClientCertExclusionPath <String>]`: meddelandeautentisering-avgränsade sökvägar för klient certifikat</span><span class="sxs-lookup"><span data-stu-id="56ef9-156">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="56ef9-157">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Program inställning åsidosätter för klonad app.</span><span class="sxs-lookup"><span data-stu-id="56ef9-157">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="56ef9-158">Om det här alternativet anges åsidosätter dessa inställningar de inställningar som klonas från käll programmet.</span><span class="sxs-lookup"><span data-stu-id="56ef9-158">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="56ef9-159">Annars sparas program inställningar från käll programmet.</span><span class="sxs-lookup"><span data-stu-id="56ef9-159">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="56ef9-160">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="56ef9-160">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="56ef9-161">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> för att klona anpassade värdnamn från käll programmet, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="56ef9-161">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="56ef9-162">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> för att klona käll kontrollen från käll programmet, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="56ef9-162">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="56ef9-163">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> för att konfigurera belastnings utjämning för käll-och mål programmet.</span><span class="sxs-lookup"><span data-stu-id="56ef9-163">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="56ef9-164">`[CloningInfoCorrelationId <String>]`: Korrelations-ID för klonings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="56ef9-164">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="56ef9-165">Detta ID bevarar flera klonings operationer tillsammans för att använda samma ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="56ef9-165">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="56ef9-166">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span><span class="sxs-lookup"><span data-stu-id="56ef9-166">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="56ef9-167">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> för att skriva över mål programmet, annars, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="56ef9-167">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="56ef9-168">`[CloningInfoSourceWebAppLocation <String>]`: Käll appens plats, t. ex.</span><span class="sxs-lookup"><span data-stu-id="56ef9-168">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="56ef9-169">`[CloningInfoTrafficManagerProfileId <String>]`: ID för den Traffic Manager-profil som ska användas, om den finns.</span><span class="sxs-lookup"><span data-stu-id="56ef9-169">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="56ef9-170">Resurs-ID för Traffic Manager har formen/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="56ef9-170">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="56ef9-171">`[CloningInfoTrafficManagerProfileName <String>]`: Namnet på Traffic Manager-profilen som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="56ef9-171">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="56ef9-172">Detta krävs endast om Traffic Manager-profilen inte redan finns.</span><span class="sxs-lookup"><span data-stu-id="56ef9-172">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="56ef9-173">`[Config <ISiteConfig>]`: Programmets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="56ef9-173">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="56ef9-174">`IsPushEnabled <Boolean>`: Hämtar eller anger en flagga som anger om push-slutpunkten är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="56ef9-174">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="56ef9-175">`[ActionMinProcessExecutionTime <String>]`: Minsta tid då processen måste utföras innan åtgärden utförs</span><span class="sxs-lookup"><span data-stu-id="56ef9-175">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="56ef9-176">`[ActionType <AutoHealActionType?>]`: Fördefinierad åtgärd som ska vidtas.</span><span class="sxs-lookup"><span data-stu-id="56ef9-176">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="56ef9-177">`[AlwaysOn <Boolean?>]`: <code>true</code> om Always On är aktiverat, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="56ef9-177">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="56ef9-178">`[ApiDefinitionUrl <String>]`: API-definitionen URL.</span><span class="sxs-lookup"><span data-stu-id="56ef9-178">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="56ef9-179">`[ApiManagementConfigId <String>]`: APIM-Api-ID.</span><span class="sxs-lookup"><span data-stu-id="56ef9-179">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="56ef9-180">`[AppCommandLine <String>]`: Programmets kommando rad för start.</span><span class="sxs-lookup"><span data-stu-id="56ef9-180">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="56ef9-181">`[AppSetting <INameValuePair[]>]`: Program inställningar.</span><span class="sxs-lookup"><span data-stu-id="56ef9-181">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="56ef9-182">`[Name <String>]`: Parets namn.</span><span class="sxs-lookup"><span data-stu-id="56ef9-182">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="56ef9-183">`[Value <String>]`: Paret.</span><span class="sxs-lookup"><span data-stu-id="56ef9-183">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="56ef9-184">`[AutoHealEnabled <Boolean?>]`: <code>true</code> om Auto läka är aktiverat, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="56ef9-184">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="56ef9-185">`[AutoSwapSlotName <String>]`: Byt plats namn automatiskt.</span><span class="sxs-lookup"><span data-stu-id="56ef9-185">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="56ef9-186">`[ConnectionString <IConnStringInfo[]>]`: Anslutnings strängar.</span><span class="sxs-lookup"><span data-stu-id="56ef9-186">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="56ef9-187">`[ConnectionString <String>]`: Anslutnings sträng värde.</span><span class="sxs-lookup"><span data-stu-id="56ef9-187">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="56ef9-188">`[Name <String>]`: Anslutnings strängens namn.</span><span class="sxs-lookup"><span data-stu-id="56ef9-188">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="56ef9-189">`[Type <ConnectionStringType?>]`: Typ av databas.</span><span class="sxs-lookup"><span data-stu-id="56ef9-189">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="56ef9-190">`[CorAllowedOrigin <String[]>]`: Hämtar eller anger listan över ursprung som ska tillåtas att ringa kors ursprung (till exempel: http://example.com:12345) .</span><span class="sxs-lookup"><span data-stu-id="56ef9-190">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="56ef9-191">Använd "\*" för att tillåta alla.</span><span class="sxs-lookup"><span data-stu-id="56ef9-191">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="56ef9-192">`[CorSupportCredentials <Boolean?>]`: Hämtar eller anger om CORS-begäranden med autentiseringsuppgifter är tillåtna.</span><span class="sxs-lookup"><span data-stu-id="56ef9-192">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="56ef9-193">Se         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         för mer information.</span><span class="sxs-lookup"><span data-stu-id="56ef9-193">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="56ef9-194">`[CustomActionExe <String>]`: Den körbara filen körs.</span><span class="sxs-lookup"><span data-stu-id="56ef9-194">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="56ef9-195">`[CustomActionParameter <String>]`: Parametrar för den körbara filen.</span><span class="sxs-lookup"><span data-stu-id="56ef9-195">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="56ef9-196">`[DefaultDocument <String[]>]`: Standard dokument.</span><span class="sxs-lookup"><span data-stu-id="56ef9-196">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="56ef9-197">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> om detaljerad fel loggning är aktive rad, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="56ef9-197">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="56ef9-198">`[DocumentRoot <String>]`: Dokument rot.</span><span class="sxs-lookup"><span data-stu-id="56ef9-198">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="56ef9-199">`[DynamicTagsJson <String>]`: Hämtar eller anger en JSON-sträng som innehåller en lista över dynamiska taggar som ska utvärderas från användar anspråk i push-registrerings slut punkten.</span><span class="sxs-lookup"><span data-stu-id="56ef9-199">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="56ef9-200">`[ExperimentRampUpRule <IRampUpRule[]>]`: Lista över regler för ramp up.</span><span class="sxs-lookup"><span data-stu-id="56ef9-200">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="56ef9-201">`[ActionHostName <String>]`: Värd namnet för en plats där trafiken ska omdirigeras om det har beslut ATS.</span><span class="sxs-lookup"><span data-stu-id="56ef9-201">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="56ef9-202">Namn@example.com.</span><span class="sxs-lookup"><span data-stu-id="56ef9-202">E.g.</span></span> <span data-ttu-id="56ef9-203">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="56ef9-203">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="56ef9-204">`[ChangeDecisionCallbackUrl <String>]`: Den anpassade besluts algoritmen kan tillhandahållas i TiPCallback som webb adress (URL) kan anges.</span><span class="sxs-lookup"><span data-stu-id="56ef9-204">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="56ef9-205">Se TiPCallback webbplats tillägg för stödjer och kontrakt.</span><span class="sxs-lookup"><span data-stu-id="56ef9-205">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="56ef9-206"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="56ef9-206">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="56ef9-207">`[ChangeIntervalInMinute <Int32?>]`: Anger intervall i minuter för att utvärdera ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="56ef9-207">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="56ef9-208">`[ChangeStep <Double?>]`: I scenario för automatisk ramp kan du lägga till/ta bort från <code>ReroutePercentage</code> tills det når \n <code>MinReroutePercentage</code> eller         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="56ef9-208">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="56ef9-209">Webbplats mått kontrol leras var N minuter som anges i <code>ChangeIntervalInMinutes</code> .\nCustom besluts algoritm kan tillhandahållas i TiPCallback webbplats tillägg som URL: en kan anges i <code>ChangeDecisionCallbackUrl</code> .</span><span class="sxs-lookup"><span data-stu-id="56ef9-209">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="56ef9-210">`[MaxReroutePercentage <Double?>]`: Anger övre gräns nedanför vilken ReroutePercentage förblir.</span><span class="sxs-lookup"><span data-stu-id="56ef9-210">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="56ef9-211">`[MinReroutePercentage <Double?>]`: Anger nedre gräns ovanför vilken ReroutePercentage blir.</span><span class="sxs-lookup"><span data-stu-id="56ef9-211">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="56ef9-212">`[Name <String>]`: Namnet på regeln.</span><span class="sxs-lookup"><span data-stu-id="56ef9-212">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="56ef9-213">Det rekommenderade namnet är att peka på den plats där trafiken tas emot i experimentet.</span><span class="sxs-lookup"><span data-stu-id="56ef9-213">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="56ef9-214">`[ReroutePercentage <Double?>]`: Procent andel av trafiken som kommer att omdirigeras till <code>ActionHostName</code> .</span><span class="sxs-lookup"><span data-stu-id="56ef9-214">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="56ef9-215">`[FtpsState <FtpsState?>]`: FTP-FTPS</span><span class="sxs-lookup"><span data-stu-id="56ef9-215">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="56ef9-216">`[HandlerMapping <IHandlerMapping[]>]`: Hanterarmappning.</span><span class="sxs-lookup"><span data-stu-id="56ef9-216">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="56ef9-217">`[Argument <String>]`: Kommando rads argument som ska överföras till skript processorn.</span><span class="sxs-lookup"><span data-stu-id="56ef9-217">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="56ef9-218">`[Extension <String>]`: Förfrågningar med den här tillägget hanteras med det angivna FastCGI-programmet.</span><span class="sxs-lookup"><span data-stu-id="56ef9-218">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="56ef9-219">`[ScriptProcessor <String>]`: Den absoluta sökvägen till FastCGI-programmet.</span><span class="sxs-lookup"><span data-stu-id="56ef9-219">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="56ef9-220">`[HealthCheckPath <String>]`: Hälso kontroll Sök väg</span><span class="sxs-lookup"><span data-stu-id="56ef9-220">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="56ef9-221">`[Http20Enabled <Boolean?>]`: Http20Enabled: konfigurerar en webbplats för att tillåta klienter att ansluta via http 2.0</span><span class="sxs-lookup"><span data-stu-id="56ef9-221">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="56ef9-222">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> om HTTP-loggning är aktiverat, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="56ef9-222">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="56ef9-223">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: Begränsningar för IP-säkerhet för huvud.</span><span class="sxs-lookup"><span data-stu-id="56ef9-223">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="56ef9-224">`[Action <String>]`: Tillåt eller neka åtkomst för detta IP-intervall.</span><span class="sxs-lookup"><span data-stu-id="56ef9-224">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="56ef9-225">`[Description <String>]`: Beskrivning för regel för IP-begränsning.</span><span class="sxs-lookup"><span data-stu-id="56ef9-225">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="56ef9-226">`[IPAddress <String>]`: IP-adress säkerhets begränsningen är giltig för.</span><span class="sxs-lookup"><span data-stu-id="56ef9-226">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="56ef9-227">Den kan vara i form av en ren IPv4-adress (obligatoriskt nätmask-egenskap) eller CIDR-notering, till exempel IPv4/mask (inledande bit träff).</span><span class="sxs-lookup"><span data-stu-id="56ef9-227">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="56ef9-228">Egenskapen nätmask måste anges.</span><span class="sxs-lookup"><span data-stu-id="56ef9-228">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="56ef9-229">`[Name <String>]`: Namn på regel för IP-begränsning.</span><span class="sxs-lookup"><span data-stu-id="56ef9-229">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="56ef9-230">`[Priority <Int32?>]`: Prioritet för IP-begränsning regeln.</span><span class="sxs-lookup"><span data-stu-id="56ef9-230">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="56ef9-231">`[SubnetMask <String>]`: Nät masken för intervallet med IP-adresser begränsningen är giltig för.</span><span class="sxs-lookup"><span data-stu-id="56ef9-231">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="56ef9-232">`[SubnetTrafficTag <Int32?>]`: (intern) kod för nät trafik</span><span class="sxs-lookup"><span data-stu-id="56ef9-232">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="56ef9-233">`[Tag <IPFilterTag?>]`: Definierar vad det här IP-filtret ska användas till.</span><span class="sxs-lookup"><span data-stu-id="56ef9-233">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="56ef9-234">Detta är till för att stödja IP-filtrering på proxyservrar.</span><span class="sxs-lookup"><span data-stu-id="56ef9-234">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="56ef9-235">`[VnetSubnetResourceId <String>]`: ID för virtuell nätverks resurs</span><span class="sxs-lookup"><span data-stu-id="56ef9-235">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="56ef9-236">`[VnetTrafficTag <Int32?>]`: (intern) tagg för VNet-trafik</span><span class="sxs-lookup"><span data-stu-id="56ef9-236">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="56ef9-237">`[JavaContainer <String>]`: Java-behållare.</span><span class="sxs-lookup"><span data-stu-id="56ef9-237">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="56ef9-238">`[JavaContainerVersion <String>]`: Java-container version.</span><span class="sxs-lookup"><span data-stu-id="56ef9-238">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="56ef9-239">`[JavaVersion <String>]`: Java-version.</span><span class="sxs-lookup"><span data-stu-id="56ef9-239">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="56ef9-240">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximal mängd disk storlek i MB.</span><span class="sxs-lookup"><span data-stu-id="56ef9-240">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="56ef9-241">`[LimitMaxMemoryInMb <Int64?>]`: Högsta tillåtna minnes användning i MB.</span><span class="sxs-lookup"><span data-stu-id="56ef9-241">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="56ef9-242">`[LimitMaxPercentageCpu <Double?>]`: Högsta tillåtna processor användnings procent.</span><span class="sxs-lookup"><span data-stu-id="56ef9-242">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="56ef9-243">`[LinuxFxVersion <String>]`: Linux program ramverk och-version</span><span class="sxs-lookup"><span data-stu-id="56ef9-243">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="56ef9-244">`[LoadBalancing <SiteLoadBalancing?>]`: Utjämning av webbplats belastning.</span><span class="sxs-lookup"><span data-stu-id="56ef9-244">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="56ef9-245">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> för att aktivera lokal MySQL; <code>false</code></span><span class="sxs-lookup"><span data-stu-id="56ef9-245">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="56ef9-246">`[LogsDirectorySizeLimit <Int32?>]`: HTTP-loggningens storleks gräns.</span><span class="sxs-lookup"><span data-stu-id="56ef9-246">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="56ef9-247">`[MachineKeyDecryption <String>]`: Algoritm som används för dekryptering.</span><span class="sxs-lookup"><span data-stu-id="56ef9-247">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="56ef9-248">`[MachineKeyDecryptionKey <String>]`: Dekrypteringsnyckel.</span><span class="sxs-lookup"><span data-stu-id="56ef9-248">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="56ef9-249">`[MachineKeyValidation <String>]`: MachineKey-verifiering.</span><span class="sxs-lookup"><span data-stu-id="56ef9-249">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="56ef9-250">`[MachineKeyValidationKey <String>]`: Verifierings tangenten.</span><span class="sxs-lookup"><span data-stu-id="56ef9-250">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="56ef9-251">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Hanterat pipeline-läge.</span><span class="sxs-lookup"><span data-stu-id="56ef9-251">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="56ef9-252">`[ManagedServiceIdentityId <Int32?>]`: ID för hanterad tjänst identitet</span><span class="sxs-lookup"><span data-stu-id="56ef9-252">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="56ef9-253">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: konfigurerar den minsta versionen av TLS som krävs för SSL-begäranden</span><span class="sxs-lookup"><span data-stu-id="56ef9-253">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="56ef9-254">`[NetFrameworkVersion <String>]`: .NET Framework-version.</span><span class="sxs-lookup"><span data-stu-id="56ef9-254">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="56ef9-255">`[NodeVersion <String>]`: Version av Node.js.</span><span class="sxs-lookup"><span data-stu-id="56ef9-255">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="56ef9-256">`[NumberOfWorker <Int32?>]`: Antal anställda.</span><span class="sxs-lookup"><span data-stu-id="56ef9-256">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="56ef9-257">`[PhpVersion <String>]`: Version av PHP.</span><span class="sxs-lookup"><span data-stu-id="56ef9-257">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="56ef9-258">`[PowerShellVersion <String>]`: Version av PowerShell.</span><span class="sxs-lookup"><span data-stu-id="56ef9-258">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="56ef9-259">`[PreWarmedInstanceCount <Int32?>]`: Antal invärmade instanser.</span><span class="sxs-lookup"><span data-stu-id="56ef9-259">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="56ef9-260">Den här inställningen gäller endast för förbrukning och elastiska abonnemang</span><span class="sxs-lookup"><span data-stu-id="56ef9-260">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="56ef9-261">`[PublishingUsername <String>]`: Publicera användar namn.</span><span class="sxs-lookup"><span data-stu-id="56ef9-261">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="56ef9-262">`[PushKind <String>]`: Typ av resurs.</span><span class="sxs-lookup"><span data-stu-id="56ef9-262">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="56ef9-263">`[PythonVersion <String>]`: Version av python.</span><span class="sxs-lookup"><span data-stu-id="56ef9-263">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="56ef9-264">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> om fjärrfelsökning är aktive rad, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="56ef9-264">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="56ef9-265">`[RemoteDebuggingVersion <String>]`: Remote debug-version.</span><span class="sxs-lookup"><span data-stu-id="56ef9-265">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="56ef9-266">`[RequestCount <Int32?>]`: Antal förfrågningar.</span><span class="sxs-lookup"><span data-stu-id="56ef9-266">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="56ef9-267">`[RequestTimeInterval <String>]`: Tidsintervall.</span><span class="sxs-lookup"><span data-stu-id="56ef9-267">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="56ef9-268">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> om spårning för förfrågningar är aktiverat, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="56ef9-268">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="56ef9-269">`[RequestTracingExpirationTime <DateTime?>]`: Spårnings tiden förfaller.</span><span class="sxs-lookup"><span data-stu-id="56ef9-269">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="56ef9-270">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-säkerhetsrestriktioner för SCM.</span><span class="sxs-lookup"><span data-stu-id="56ef9-270">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="56ef9-271">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP-säkerhetsrestriktioner för SCM för att använda main.</span><span class="sxs-lookup"><span data-stu-id="56ef9-271">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="56ef9-272">`[ScmType <ScmType?>]`: SCM-typ.</span><span class="sxs-lookup"><span data-stu-id="56ef9-272">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="56ef9-273">`[SlowRequestCount <Int32?>]`: Antal förfrågningar.</span><span class="sxs-lookup"><span data-stu-id="56ef9-273">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="56ef9-274">`[SlowRequestTimeInterval <String>]`: Tidsintervall.</span><span class="sxs-lookup"><span data-stu-id="56ef9-274">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="56ef9-275">`[SlowRequestTimeTaken <String>]`: Åtgången tid.</span><span class="sxs-lookup"><span data-stu-id="56ef9-275">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="56ef9-276">`[TagWhitelistJson <String>]`: Hämtar eller anger en JSON-sträng som innehåller en lista med taggar som är whitelisted för användning av push-registrerings slut punkten.</span><span class="sxs-lookup"><span data-stu-id="56ef9-276">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="56ef9-277">`[TagsRequiringAuth <String>]`: Hämtar eller anger en JSON-sträng som innehåller en lista med taggar som kräver att användarautentisering används i push-registrerings slut punkten.</span><span class="sxs-lookup"><span data-stu-id="56ef9-277">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="56ef9-278">Taggar kan bestå av alfanumeriska tecken och följande: "_", "@", "#", ".", ":", "-".</span><span class="sxs-lookup"><span data-stu-id="56ef9-278">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="56ef9-279">Verifiering ska utföras på PushRequestHandler.</span><span class="sxs-lookup"><span data-stu-id="56ef9-279">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="56ef9-280">`[TracingOption <String>]`: Spårnings alternativ.</span><span class="sxs-lookup"><span data-stu-id="56ef9-280">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="56ef9-281">`[TriggerPrivateBytesInKb <Int32?>]`: En regel baserad på privata byte.</span><span class="sxs-lookup"><span data-stu-id="56ef9-281">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="56ef9-282">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: En regel baserad på status koder.</span><span class="sxs-lookup"><span data-stu-id="56ef9-282">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="56ef9-283">`[Count <Int32?>]`: Antal förfrågningar.</span><span class="sxs-lookup"><span data-stu-id="56ef9-283">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="56ef9-284">`[Status <Int32?>]`: HTTP-statuskod.</span><span class="sxs-lookup"><span data-stu-id="56ef9-284">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="56ef9-285">`[SubStatus <Int32?>]`: Under status för begäran.</span><span class="sxs-lookup"><span data-stu-id="56ef9-285">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="56ef9-286">`[TimeInterval <String>]`: Tidsintervall.</span><span class="sxs-lookup"><span data-stu-id="56ef9-286">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="56ef9-287">`[Win32Status <Int32?>]`: Win32-felkod.</span><span class="sxs-lookup"><span data-stu-id="56ef9-287">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="56ef9-288">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> för att använda 32-bitars arbets process, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="56ef9-288">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="56ef9-289">`[VirtualApplication <IVirtualApplication[]>]`: Virtuella program.</span><span class="sxs-lookup"><span data-stu-id="56ef9-289">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="56ef9-290">`[PhysicalPath <String>]`: Fysisk sökväg.</span><span class="sxs-lookup"><span data-stu-id="56ef9-290">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="56ef9-291">`[PreloadEnabled <Boolean?>]`: <code>true</code> om för inläsning är aktiverat, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="56ef9-291">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="56ef9-292">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtuella kataloger för virtuella program.</span><span class="sxs-lookup"><span data-stu-id="56ef9-292">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="56ef9-293">`[PhysicalPath <String>]`: Fysisk sökväg.</span><span class="sxs-lookup"><span data-stu-id="56ef9-293">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="56ef9-294">`[VirtualPath <String>]`: Sökväg till virtuellt program.</span><span class="sxs-lookup"><span data-stu-id="56ef9-294">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="56ef9-295">`[VirtualPath <String>]`: Virtuell sökväg.</span><span class="sxs-lookup"><span data-stu-id="56ef9-295">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="56ef9-296">`[VnetName <String>]`: Virtuellt nätverks namn.</span><span class="sxs-lookup"><span data-stu-id="56ef9-296">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="56ef9-297">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> om WebSocket är aktiverat, annars, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="56ef9-297">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="56ef9-298">`[WindowsFxVersion <String>]`: Xenon program ramverk och-version</span><span class="sxs-lookup"><span data-stu-id="56ef9-298">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="56ef9-299">`[XManagedServiceIdentityId <Int32?>]`: Explicit hanterat identitets-ID</span><span class="sxs-lookup"><span data-stu-id="56ef9-299">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="56ef9-300">`[ContainerSize <Int32?>]`: Funktions behållaens storlek.</span><span class="sxs-lookup"><span data-stu-id="56ef9-300">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="56ef9-301">`[DailyMemoryTimeQuota <Int32?>]`: Högsta tillåtna mängd minne – tids kvot (gäller endast dynamiska program).</span><span class="sxs-lookup"><span data-stu-id="56ef9-301">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="56ef9-302">`[Enabled <Boolean?>]`: <code>true</code> om appen är aktive rad, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="56ef9-302">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="56ef9-303">Om du anger det här värdet till false inaktive ras programmet (tar programmet offline).</span><span class="sxs-lookup"><span data-stu-id="56ef9-303">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="56ef9-304">`[HostNameSslState <IHostNameSslState[]>]`: Hostname för SSL-tillstånd används för att hantera SSL-bindningar för programmets värdnamn.</span><span class="sxs-lookup"><span data-stu-id="56ef9-304">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="56ef9-305">`[HostType <HostType?>]`: Anger om värd namnet är en standard-eller databas värd.</span><span class="sxs-lookup"><span data-stu-id="56ef9-305">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="56ef9-306">`[Name <String>]`Namn.</span><span class="sxs-lookup"><span data-stu-id="56ef9-306">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="56ef9-307">`[SslState <SslState?>]`: SSL-typ.</span><span class="sxs-lookup"><span data-stu-id="56ef9-307">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="56ef9-308">`[Thumbprint <String>]`: Tumavtryck för SSL-certifikat.</span><span class="sxs-lookup"><span data-stu-id="56ef9-308">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="56ef9-309">`[ToUpdate <Boolean?>]`: Angett för <code>true</code> att uppdatera befintligt värdnamn.</span><span class="sxs-lookup"><span data-stu-id="56ef9-309">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="56ef9-310">`[VirtualIP <String>]`: Virtuell IP-adress som tilldelats värd namnet om IP-baserad SSL är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="56ef9-310">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="56ef9-311">`[HostNamesDisabled <Boolean?>]`: <code>true</code> så här inaktiverar du de offentliga värdarna för appen, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="56ef9-311">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="56ef9-312">Om <code>true</code> programmet endast är tillgängligt via API Management process.</span><span class="sxs-lookup"><span data-stu-id="56ef9-312">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="56ef9-313">`[HostingEnvironmentProfileId <String>]`: Resurs-ID för App Service Environment.</span><span class="sxs-lookup"><span data-stu-id="56ef9-313">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="56ef9-314">`[HttpsOnly <Boolean?>]`: HttpsOnly: konfigurerar en webbplats för att acceptera endast HTTPS-begäranden.</span><span class="sxs-lookup"><span data-stu-id="56ef9-314">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="56ef9-315">Problem vid omdirigering för HTTP-begäranden</span><span class="sxs-lookup"><span data-stu-id="56ef9-315">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="56ef9-316">`[HyperV <Boolean?>]`: Hyper-V Sand låda.</span><span class="sxs-lookup"><span data-stu-id="56ef9-316">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="56ef9-317">`[IdentityType <ManagedServiceIdentityType?>]`: Typen av hanterad tjänst identitet.</span><span class="sxs-lookup"><span data-stu-id="56ef9-317">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="56ef9-318">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Listan med användare tilldelade identiteter associerade med resursen.</span><span class="sxs-lookup"><span data-stu-id="56ef9-318">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="56ef9-319">Nyckelorden för användar identitets ord lista kommer att vara resurs-ID: n i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="56ef9-319">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="56ef9-320">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="56ef9-320">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="56ef9-321">`[IsXenon <Boolean?>]`: Överflödig: Sand låda för Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="56ef9-321">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="56ef9-322">`[RedundancyMode <RedundancyMode?>]`: Läget för webbplats redundans</span><span class="sxs-lookup"><span data-stu-id="56ef9-322">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="56ef9-323">`[Reserved <Boolean?>]`: <code>true</code> om det reserveras; annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="56ef9-323">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="56ef9-324">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> stoppa SCM (kudu)-webbplatsen när appen stoppas, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="56ef9-324">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="56ef9-325">Standardvärdet är <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="56ef9-325">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="56ef9-326">`[ServerFarmId <String>]`: Resurs-ID för den associerade App Service-planen, formaterad som: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="56ef9-326">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="56ef9-327">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="56ef9-327">RELATED LINKS</span></span>

