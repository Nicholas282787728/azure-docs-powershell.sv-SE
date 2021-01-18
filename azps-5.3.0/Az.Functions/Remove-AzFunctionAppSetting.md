---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppSetting.md
ms.openlocfilehash: abfa704b042b0a8cd25b8682e3b93306b5ca6277
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520676"
---
# <span data-ttu-id="fde50-101">Remove-AzFunctionAppSetting</span><span class="sxs-lookup"><span data-stu-id="fde50-101">Remove-AzFunctionAppSetting</span></span>

## <span data-ttu-id="fde50-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fde50-102">SYNOPSIS</span></span>
<span data-ttu-id="fde50-103">Tar bort program inställningar från ett Function-program.</span><span class="sxs-lookup"><span data-stu-id="fde50-103">Removes app settings from a function app.</span></span>

## <span data-ttu-id="fde50-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fde50-104">SYNTAX</span></span>

### <span data-ttu-id="fde50-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="fde50-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> -AppSettingName <String[]>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fde50-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="fde50-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppSetting -AppSettingName <String[]> -InputObject <ISite> [-Force]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fde50-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fde50-107">DESCRIPTION</span></span>
<span data-ttu-id="fde50-108">Tar bort program inställningar från ett Function-program.</span><span class="sxs-lookup"><span data-stu-id="fde50-108">Removes app settings from a function app.</span></span>

## <span data-ttu-id="fde50-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fde50-109">EXAMPLES</span></span>

### <span data-ttu-id="fde50-110">Exempel 1: ta bort appinställningar i ett Function-program.</span><span class="sxs-lookup"><span data-stu-id="fde50-110">Example 1: Remove app settings in a function app.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName -AppSettingName "MyAppSetting1", "MyAppSetting2"
```

<span data-ttu-id="fde50-111">Det här kommandot tar bort program inställningar i ett Function-program.</span><span class="sxs-lookup"><span data-stu-id="fde50-111">This command removes app settings in a function app.</span></span>

## <span data-ttu-id="fde50-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fde50-112">PARAMETERS</span></span>

### <span data-ttu-id="fde50-113">-AppSettingName</span><span class="sxs-lookup"><span data-stu-id="fde50-113">-AppSettingName</span></span>
<span data-ttu-id="fde50-114">Lista över inställningar för funktionalitet som ska tas bort från programmet funktion.</span><span class="sxs-lookup"><span data-stu-id="fde50-114">List of function app settings to be removed from the function app.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde50-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fde50-115">-DefaultProfile</span></span>


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

### <span data-ttu-id="fde50-116">-Force</span><span class="sxs-lookup"><span data-stu-id="fde50-116">-Force</span></span>
<span data-ttu-id="fde50-117">Tvingar cmdleten att ta bort programinställning utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="fde50-117">Forces the cmdlet to remove function app setting without prompting for confirmation.</span></span>

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

### <span data-ttu-id="fde50-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fde50-118">-InputObject</span></span>
<span data-ttu-id="fde50-119">För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="fde50-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fde50-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="fde50-120">-Name</span></span>
<span data-ttu-id="fde50-121">Namnet på funktionen funktion.</span><span class="sxs-lookup"><span data-stu-id="fde50-121">Name of the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde50-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fde50-122">-ResourceGroupName</span></span>
<span data-ttu-id="fde50-123">Namnet på den resurs grupp som resursen tillhör.</span><span class="sxs-lookup"><span data-stu-id="fde50-123">Name of the resource group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde50-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fde50-124">-SubscriptionId</span></span>
<span data-ttu-id="fde50-125">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="fde50-125">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fde50-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fde50-126">-Confirm</span></span>
<span data-ttu-id="fde50-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fde50-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fde50-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fde50-128">-WhatIf</span></span>
<span data-ttu-id="fde50-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fde50-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fde50-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fde50-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fde50-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fde50-131">CommonParameters</span></span>
<span data-ttu-id="fde50-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fde50-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fde50-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fde50-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fde50-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fde50-134">INPUTS</span></span>

### <span data-ttu-id="fde50-135">Microsoft. Azure. PowerShell. cmdletar. functions. Models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="fde50-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="fde50-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fde50-136">OUTPUTS</span></span>

### <span data-ttu-id="fde50-137">Microsoft. Azure. PowerShell. cmdletar. functions. Models. Api20190801. IStringDictionary</span><span class="sxs-lookup"><span data-stu-id="fde50-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span></span>

## <span data-ttu-id="fde50-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fde50-138">NOTES</span></span>

<span data-ttu-id="fde50-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="fde50-139">ALIASES</span></span>

<span data-ttu-id="fde50-140">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="fde50-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fde50-141">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="fde50-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fde50-142">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fde50-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fde50-143">INPUTOBJECT <ISite> :</span><span class="sxs-lookup"><span data-stu-id="fde50-143">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="fde50-144">`Location <String>`: Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="fde50-144">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="fde50-145">`CloningInfoSourceWebAppId <String>`: Käll programmets ID för ARM-resurs.</span><span class="sxs-lookup"><span data-stu-id="fde50-145">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="fde50-146">App-resurs-ID är/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} för produktions platser och/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} för andra platser.</span><span class="sxs-lookup"><span data-stu-id="fde50-146">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="fde50-147">`[Kind <String>]`: Typ av resurs.</span><span class="sxs-lookup"><span data-stu-id="fde50-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="fde50-148">`[Tag <IResourceTags>]`: Resursfiler.</span><span class="sxs-lookup"><span data-stu-id="fde50-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="fde50-149">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="fde50-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="fde50-150">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> så här aktiverar du klient tillhörighet <code>false</code> för att sluta skicka cookie-cookies, som dirigerar klienter i samma session till samma instans.</span><span class="sxs-lookup"><span data-stu-id="fde50-150">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="fde50-151">Standard är <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="fde50-151">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="fde50-152">`[ClientCertEnabled <Boolean?>]`: <code>true</code> så här aktiverar du klientautentisering för klient certifikat (gemensam TLS-verifikation), annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fde50-152">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="fde50-153">Standard är <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fde50-153">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="fde50-154">`[ClientCertExclusionPath <String>]`: meddelandeautentisering-avgränsade sökvägar för klient certifikat</span><span class="sxs-lookup"><span data-stu-id="fde50-154">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="fde50-155">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Program inställning åsidosätter för klonad app.</span><span class="sxs-lookup"><span data-stu-id="fde50-155">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="fde50-156">Om det här alternativet anges åsidosätter dessa inställningar de inställningar som klonas från käll programmet.</span><span class="sxs-lookup"><span data-stu-id="fde50-156">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="fde50-157">Annars sparas program inställningar från käll programmet.</span><span class="sxs-lookup"><span data-stu-id="fde50-157">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="fde50-158">`[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="fde50-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="fde50-159">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> för att klona anpassade värdnamn från käll programmet, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fde50-159">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="fde50-160">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> för att klona käll kontrollen från käll programmet, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fde50-160">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="fde50-161">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> för att konfigurera belastnings utjämning för käll-och mål programmet.</span><span class="sxs-lookup"><span data-stu-id="fde50-161">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="fde50-162">`[CloningInfoCorrelationId <String>]`: Korrelations-ID för klonings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="fde50-162">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="fde50-163">Detta ID bevarar flera klonings operationer tillsammans för att använda samma ögonblicks bild.</span><span class="sxs-lookup"><span data-stu-id="fde50-163">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="fde50-164">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span><span class="sxs-lookup"><span data-stu-id="fde50-164">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="fde50-165">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> för att skriva över mål programmet, annars, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fde50-165">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="fde50-166">`[CloningInfoSourceWebAppLocation <String>]`: Käll appens plats, t. ex.</span><span class="sxs-lookup"><span data-stu-id="fde50-166">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="fde50-167">`[CloningInfoTrafficManagerProfileId <String>]`: ID för den Traffic Manager-profil som ska användas, om den finns.</span><span class="sxs-lookup"><span data-stu-id="fde50-167">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="fde50-168">Resurs-ID för Traffic Manager har formen/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="fde50-168">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="fde50-169">`[CloningInfoTrafficManagerProfileName <String>]`: Namnet på Traffic Manager-profilen som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="fde50-169">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="fde50-170">Detta krävs endast om Traffic Manager-profilen inte redan finns.</span><span class="sxs-lookup"><span data-stu-id="fde50-170">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="fde50-171">`[Config <ISiteConfig>]`: Programmets konfiguration.</span><span class="sxs-lookup"><span data-stu-id="fde50-171">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="fde50-172">`IsPushEnabled <Boolean>`: Hämtar eller anger en flagga som anger om push-slutpunkten är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="fde50-172">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="fde50-173">`[ActionMinProcessExecutionTime <String>]`: Minsta tid då processen måste utföras innan åtgärden utförs</span><span class="sxs-lookup"><span data-stu-id="fde50-173">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="fde50-174">`[ActionType <AutoHealActionType?>]`: Fördefinierad åtgärd som ska vidtas.</span><span class="sxs-lookup"><span data-stu-id="fde50-174">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="fde50-175">`[AlwaysOn <Boolean?>]`: <code>true</code> om Always On är aktiverat, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fde50-175">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="fde50-176">`[ApiDefinitionUrl <String>]`: API-definitionen URL.</span><span class="sxs-lookup"><span data-stu-id="fde50-176">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="fde50-177">`[ApiManagementConfigId <String>]`: APIM-Api-ID.</span><span class="sxs-lookup"><span data-stu-id="fde50-177">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="fde50-178">`[AppCommandLine <String>]`: Programmets kommando rad för start.</span><span class="sxs-lookup"><span data-stu-id="fde50-178">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="fde50-179">`[AppSetting <INameValuePair[]>]`: Program inställningar.</span><span class="sxs-lookup"><span data-stu-id="fde50-179">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="fde50-180">`[Name <String>]`: Parets namn.</span><span class="sxs-lookup"><span data-stu-id="fde50-180">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="fde50-181">`[Value <String>]`: Paret.</span><span class="sxs-lookup"><span data-stu-id="fde50-181">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="fde50-182">`[AutoHealEnabled <Boolean?>]`: <code>true</code> om Auto läka är aktiverat, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fde50-182">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="fde50-183">`[AutoSwapSlotName <String>]`: Byt plats namn automatiskt.</span><span class="sxs-lookup"><span data-stu-id="fde50-183">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="fde50-184">`[ConnectionString <IConnStringInfo[]>]`: Anslutnings strängar.</span><span class="sxs-lookup"><span data-stu-id="fde50-184">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="fde50-185">`[ConnectionString <String>]`: Anslutnings sträng värde.</span><span class="sxs-lookup"><span data-stu-id="fde50-185">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="fde50-186">`[Name <String>]`: Anslutnings strängens namn.</span><span class="sxs-lookup"><span data-stu-id="fde50-186">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="fde50-187">`[Type <ConnectionStringType?>]`: Typ av databas.</span><span class="sxs-lookup"><span data-stu-id="fde50-187">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="fde50-188">`[CorAllowedOrigin <String[]>]`: Hämtar eller anger listan över ursprung som ska tillåtas att ringa kors ursprung (till exempel: http://example.com:12345) .</span><span class="sxs-lookup"><span data-stu-id="fde50-188">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="fde50-189">Använd "\*" för att tillåta alla.</span><span class="sxs-lookup"><span data-stu-id="fde50-189">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="fde50-190">`[CorSupportCredentials <Boolean?>]`: Hämtar eller anger om CORS-begäranden med autentiseringsuppgifter är tillåtna.</span><span class="sxs-lookup"><span data-stu-id="fde50-190">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="fde50-191">Se         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         för mer information.</span><span class="sxs-lookup"><span data-stu-id="fde50-191">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="fde50-192">`[CustomActionExe <String>]`: Den körbara filen körs.</span><span class="sxs-lookup"><span data-stu-id="fde50-192">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="fde50-193">`[CustomActionParameter <String>]`: Parametrar för den körbara filen.</span><span class="sxs-lookup"><span data-stu-id="fde50-193">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="fde50-194">`[DefaultDocument <String[]>]`: Standard dokument.</span><span class="sxs-lookup"><span data-stu-id="fde50-194">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="fde50-195">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> om detaljerad fel loggning är aktive rad, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fde50-195">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="fde50-196">`[DocumentRoot <String>]`: Dokument rot.</span><span class="sxs-lookup"><span data-stu-id="fde50-196">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="fde50-197">`[DynamicTagsJson <String>]`: Hämtar eller anger en JSON-sträng som innehåller en lista över dynamiska taggar som ska utvärderas från användar anspråk i push-registrerings slut punkten.</span><span class="sxs-lookup"><span data-stu-id="fde50-197">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="fde50-198">`[ExperimentRampUpRule <IRampUpRule[]>]`: Lista över regler för ramp up.</span><span class="sxs-lookup"><span data-stu-id="fde50-198">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="fde50-199">`[ActionHostName <String>]`: Värd namnet för en plats där trafiken ska omdirigeras om det har beslut ATS.</span><span class="sxs-lookup"><span data-stu-id="fde50-199">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="fde50-200">Namn@example.com.</span><span class="sxs-lookup"><span data-stu-id="fde50-200">E.g.</span></span> <span data-ttu-id="fde50-201">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="fde50-201">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="fde50-202">`[ChangeDecisionCallbackUrl <String>]`: Den anpassade besluts algoritmen kan tillhandahållas i TiPCallback som webb adress (URL) kan anges.</span><span class="sxs-lookup"><span data-stu-id="fde50-202">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="fde50-203">Se TiPCallback webbplats tillägg för stödjer och kontrakt.</span><span class="sxs-lookup"><span data-stu-id="fde50-203">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="fde50-204"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="fde50-204">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="fde50-205">`[ChangeIntervalInMinute <Int32?>]`: Anger intervall i minuter för att utvärdera ReroutePercentage.</span><span class="sxs-lookup"><span data-stu-id="fde50-205">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="fde50-206">`[ChangeStep <Double?>]`: I scenario för automatisk ramp kan du lägga till/ta bort från <code>ReroutePercentage</code> tills det når \n <code>MinReroutePercentage</code> eller         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="fde50-206">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="fde50-207">Webbplats mått kontrol leras var N minuter som anges i <code>ChangeIntervalInMinutes</code> .\nCustom besluts algoritm kan tillhandahållas i TiPCallback webbplats tillägg som URL: en kan anges i <code>ChangeDecisionCallbackUrl</code> .</span><span class="sxs-lookup"><span data-stu-id="fde50-207">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="fde50-208">`[MaxReroutePercentage <Double?>]`: Anger övre gräns nedanför vilken ReroutePercentage förblir.</span><span class="sxs-lookup"><span data-stu-id="fde50-208">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="fde50-209">`[MinReroutePercentage <Double?>]`: Anger nedre gräns ovanför vilken ReroutePercentage blir.</span><span class="sxs-lookup"><span data-stu-id="fde50-209">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="fde50-210">`[Name <String>]`: Namnet på regeln.</span><span class="sxs-lookup"><span data-stu-id="fde50-210">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="fde50-211">Det rekommenderade namnet är att peka på den plats där trafiken tas emot i experimentet.</span><span class="sxs-lookup"><span data-stu-id="fde50-211">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="fde50-212">`[ReroutePercentage <Double?>]`: Procent andel av trafiken som kommer att omdirigeras till <code>ActionHostName</code> .</span><span class="sxs-lookup"><span data-stu-id="fde50-212">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="fde50-213">`[FtpsState <FtpsState?>]`: FTP-FTPS</span><span class="sxs-lookup"><span data-stu-id="fde50-213">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="fde50-214">`[HandlerMapping <IHandlerMapping[]>]`: Hanterarmappning.</span><span class="sxs-lookup"><span data-stu-id="fde50-214">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="fde50-215">`[Argument <String>]`: Kommando rads argument som ska överföras till skript processorn.</span><span class="sxs-lookup"><span data-stu-id="fde50-215">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="fde50-216">`[Extension <String>]`: Förfrågningar med den här tillägget hanteras med det angivna FastCGI-programmet.</span><span class="sxs-lookup"><span data-stu-id="fde50-216">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="fde50-217">`[ScriptProcessor <String>]`: Den absoluta sökvägen till FastCGI-programmet.</span><span class="sxs-lookup"><span data-stu-id="fde50-217">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="fde50-218">`[HealthCheckPath <String>]`: Hälso kontroll Sök väg</span><span class="sxs-lookup"><span data-stu-id="fde50-218">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="fde50-219">`[Http20Enabled <Boolean?>]`: Http20Enabled: konfigurerar en webbplats för att tillåta klienter att ansluta via http 2.0</span><span class="sxs-lookup"><span data-stu-id="fde50-219">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="fde50-220">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> om HTTP-loggning är aktiverat, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fde50-220">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="fde50-221">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: Begränsningar för IP-säkerhet för huvud.</span><span class="sxs-lookup"><span data-stu-id="fde50-221">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="fde50-222">`[Action <String>]`: Tillåt eller neka åtkomst för detta IP-intervall.</span><span class="sxs-lookup"><span data-stu-id="fde50-222">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="fde50-223">`[Description <String>]`: Beskrivning för regel för IP-begränsning.</span><span class="sxs-lookup"><span data-stu-id="fde50-223">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="fde50-224">`[IPAddress <String>]`: IP-adress säkerhets begränsningen är giltig för.</span><span class="sxs-lookup"><span data-stu-id="fde50-224">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="fde50-225">Den kan vara i form av en ren IPv4-adress (obligatoriskt nätmask-egenskap) eller CIDR-notering, till exempel IPv4/mask (inledande bit träff).</span><span class="sxs-lookup"><span data-stu-id="fde50-225">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="fde50-226">Egenskapen nätmask måste anges.</span><span class="sxs-lookup"><span data-stu-id="fde50-226">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="fde50-227">`[Name <String>]`: Namn på regel för IP-begränsning.</span><span class="sxs-lookup"><span data-stu-id="fde50-227">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="fde50-228">`[Priority <Int32?>]`: Prioritet för IP-begränsning regeln.</span><span class="sxs-lookup"><span data-stu-id="fde50-228">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="fde50-229">`[SubnetMask <String>]`: Nät masken för intervallet med IP-adresser begränsningen är giltig för.</span><span class="sxs-lookup"><span data-stu-id="fde50-229">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="fde50-230">`[SubnetTrafficTag <Int32?>]`: (intern) kod för nät trafik</span><span class="sxs-lookup"><span data-stu-id="fde50-230">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="fde50-231">`[Tag <IPFilterTag?>]`: Definierar vad det här IP-filtret ska användas till.</span><span class="sxs-lookup"><span data-stu-id="fde50-231">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="fde50-232">Detta är till för att stödja IP-filtrering på proxyservrar.</span><span class="sxs-lookup"><span data-stu-id="fde50-232">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="fde50-233">`[VnetSubnetResourceId <String>]`: ID för virtuell nätverks resurs</span><span class="sxs-lookup"><span data-stu-id="fde50-233">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="fde50-234">`[VnetTrafficTag <Int32?>]`: (intern) tagg för VNet-trafik</span><span class="sxs-lookup"><span data-stu-id="fde50-234">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="fde50-235">`[JavaContainer <String>]`: Java-behållare.</span><span class="sxs-lookup"><span data-stu-id="fde50-235">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="fde50-236">`[JavaContainerVersion <String>]`: Java-container version.</span><span class="sxs-lookup"><span data-stu-id="fde50-236">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="fde50-237">`[JavaVersion <String>]`: Java-version.</span><span class="sxs-lookup"><span data-stu-id="fde50-237">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="fde50-238">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximal mängd disk storlek i MB.</span><span class="sxs-lookup"><span data-stu-id="fde50-238">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="fde50-239">`[LimitMaxMemoryInMb <Int64?>]`: Högsta tillåtna minnes användning i MB.</span><span class="sxs-lookup"><span data-stu-id="fde50-239">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="fde50-240">`[LimitMaxPercentageCpu <Double?>]`: Högsta tillåtna processor användnings procent.</span><span class="sxs-lookup"><span data-stu-id="fde50-240">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="fde50-241">`[LinuxFxVersion <String>]`: Linux program ramverk och-version</span><span class="sxs-lookup"><span data-stu-id="fde50-241">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="fde50-242">`[LoadBalancing <SiteLoadBalancing?>]`: Utjämning av webbplats belastning.</span><span class="sxs-lookup"><span data-stu-id="fde50-242">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="fde50-243">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> för att aktivera lokal MySQL; <code>false</code></span><span class="sxs-lookup"><span data-stu-id="fde50-243">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="fde50-244">`[LogsDirectorySizeLimit <Int32?>]`: HTTP-loggningens storleks gräns.</span><span class="sxs-lookup"><span data-stu-id="fde50-244">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="fde50-245">`[MachineKeyDecryption <String>]`: Algoritm som används för dekryptering.</span><span class="sxs-lookup"><span data-stu-id="fde50-245">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="fde50-246">`[MachineKeyDecryptionKey <String>]`: Dekrypteringsnyckel.</span><span class="sxs-lookup"><span data-stu-id="fde50-246">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="fde50-247">`[MachineKeyValidation <String>]`: MachineKey-verifiering.</span><span class="sxs-lookup"><span data-stu-id="fde50-247">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="fde50-248">`[MachineKeyValidationKey <String>]`: Verifierings tangenten.</span><span class="sxs-lookup"><span data-stu-id="fde50-248">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="fde50-249">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Hanterat pipeline-läge.</span><span class="sxs-lookup"><span data-stu-id="fde50-249">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="fde50-250">`[ManagedServiceIdentityId <Int32?>]`: ID för hanterad tjänst identitet</span><span class="sxs-lookup"><span data-stu-id="fde50-250">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="fde50-251">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: konfigurerar den minsta versionen av TLS som krävs för SSL-begäranden</span><span class="sxs-lookup"><span data-stu-id="fde50-251">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="fde50-252">`[NetFrameworkVersion <String>]`: .NET Framework-version.</span><span class="sxs-lookup"><span data-stu-id="fde50-252">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="fde50-253">`[NodeVersion <String>]`: Version av Node.js.</span><span class="sxs-lookup"><span data-stu-id="fde50-253">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="fde50-254">`[NumberOfWorker <Int32?>]`: Antal anställda.</span><span class="sxs-lookup"><span data-stu-id="fde50-254">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="fde50-255">`[PhpVersion <String>]`: Version av PHP.</span><span class="sxs-lookup"><span data-stu-id="fde50-255">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="fde50-256">`[PowerShellVersion <String>]`: Version av PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fde50-256">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="fde50-257">`[PreWarmedInstanceCount <Int32?>]`: Antal invärmade instanser.</span><span class="sxs-lookup"><span data-stu-id="fde50-257">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="fde50-258">Den här inställningen gäller endast för förbrukning och elastiska abonnemang</span><span class="sxs-lookup"><span data-stu-id="fde50-258">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="fde50-259">`[PublishingUsername <String>]`: Publicera användar namn.</span><span class="sxs-lookup"><span data-stu-id="fde50-259">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="fde50-260">`[PushKind <String>]`: Typ av resurs.</span><span class="sxs-lookup"><span data-stu-id="fde50-260">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="fde50-261">`[PythonVersion <String>]`: Version av python.</span><span class="sxs-lookup"><span data-stu-id="fde50-261">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="fde50-262">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> om fjärrfelsökning är aktive rad, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fde50-262">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="fde50-263">`[RemoteDebuggingVersion <String>]`: Remote debug-version.</span><span class="sxs-lookup"><span data-stu-id="fde50-263">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="fde50-264">`[RequestCount <Int32?>]`: Antal förfrågningar.</span><span class="sxs-lookup"><span data-stu-id="fde50-264">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="fde50-265">`[RequestTimeInterval <String>]`: Tidsintervall.</span><span class="sxs-lookup"><span data-stu-id="fde50-265">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="fde50-266">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> om spårning för förfrågningar är aktiverat, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fde50-266">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="fde50-267">`[RequestTracingExpirationTime <DateTime?>]`: Spårnings tiden förfaller.</span><span class="sxs-lookup"><span data-stu-id="fde50-267">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="fde50-268">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-säkerhetsrestriktioner för SCM.</span><span class="sxs-lookup"><span data-stu-id="fde50-268">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="fde50-269">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP-säkerhetsrestriktioner för SCM för att använda main.</span><span class="sxs-lookup"><span data-stu-id="fde50-269">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="fde50-270">`[ScmType <ScmType?>]`: SCM-typ.</span><span class="sxs-lookup"><span data-stu-id="fde50-270">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="fde50-271">`[SlowRequestCount <Int32?>]`: Antal förfrågningar.</span><span class="sxs-lookup"><span data-stu-id="fde50-271">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="fde50-272">`[SlowRequestTimeInterval <String>]`: Tidsintervall.</span><span class="sxs-lookup"><span data-stu-id="fde50-272">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="fde50-273">`[SlowRequestTimeTaken <String>]`: Åtgången tid.</span><span class="sxs-lookup"><span data-stu-id="fde50-273">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="fde50-274">`[TagWhitelistJson <String>]`: Hämtar eller anger en JSON-sträng som innehåller en lista med taggar som är whitelisted för användning av push-registrerings slut punkten.</span><span class="sxs-lookup"><span data-stu-id="fde50-274">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="fde50-275">`[TagsRequiringAuth <String>]`: Hämtar eller anger en JSON-sträng som innehåller en lista med taggar som kräver att användarautentisering används i push-registrerings slut punkten.</span><span class="sxs-lookup"><span data-stu-id="fde50-275">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="fde50-276">Taggar kan bestå av alfanumeriska tecken och följande: "_", "@", "#", ".", ":", "-".</span><span class="sxs-lookup"><span data-stu-id="fde50-276">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="fde50-277">Verifiering ska utföras på PushRequestHandler.</span><span class="sxs-lookup"><span data-stu-id="fde50-277">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="fde50-278">`[TracingOption <String>]`: Spårnings alternativ.</span><span class="sxs-lookup"><span data-stu-id="fde50-278">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="fde50-279">`[TriggerPrivateBytesInKb <Int32?>]`: En regel baserad på privata byte.</span><span class="sxs-lookup"><span data-stu-id="fde50-279">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="fde50-280">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: En regel baserad på status koder.</span><span class="sxs-lookup"><span data-stu-id="fde50-280">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="fde50-281">`[Count <Int32?>]`: Antal förfrågningar.</span><span class="sxs-lookup"><span data-stu-id="fde50-281">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="fde50-282">`[Status <Int32?>]`: HTTP-statuskod.</span><span class="sxs-lookup"><span data-stu-id="fde50-282">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="fde50-283">`[SubStatus <Int32?>]`: Under status för begäran.</span><span class="sxs-lookup"><span data-stu-id="fde50-283">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="fde50-284">`[TimeInterval <String>]`: Tidsintervall.</span><span class="sxs-lookup"><span data-stu-id="fde50-284">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="fde50-285">`[Win32Status <Int32?>]`: Win32-felkod.</span><span class="sxs-lookup"><span data-stu-id="fde50-285">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="fde50-286">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> för att använda 32-bitars arbets process, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fde50-286">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="fde50-287">`[VirtualApplication <IVirtualApplication[]>]`: Virtuella program.</span><span class="sxs-lookup"><span data-stu-id="fde50-287">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="fde50-288">`[PhysicalPath <String>]`: Fysisk sökväg.</span><span class="sxs-lookup"><span data-stu-id="fde50-288">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="fde50-289">`[PreloadEnabled <Boolean?>]`: <code>true</code> om för inläsning är aktiverat, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fde50-289">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="fde50-290">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtuella kataloger för virtuella program.</span><span class="sxs-lookup"><span data-stu-id="fde50-290">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="fde50-291">`[PhysicalPath <String>]`: Fysisk sökväg.</span><span class="sxs-lookup"><span data-stu-id="fde50-291">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="fde50-292">`[VirtualPath <String>]`: Sökväg till virtuellt program.</span><span class="sxs-lookup"><span data-stu-id="fde50-292">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="fde50-293">`[VirtualPath <String>]`: Virtuell sökväg.</span><span class="sxs-lookup"><span data-stu-id="fde50-293">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="fde50-294">`[VnetName <String>]`: Virtuellt nätverks namn.</span><span class="sxs-lookup"><span data-stu-id="fde50-294">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="fde50-295">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> om WebSocket är aktiverat, annars, <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fde50-295">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="fde50-296">`[WindowsFxVersion <String>]`: Xenon program ramverk och-version</span><span class="sxs-lookup"><span data-stu-id="fde50-296">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="fde50-297">`[XManagedServiceIdentityId <Int32?>]`: Explicit hanterat identitets-ID</span><span class="sxs-lookup"><span data-stu-id="fde50-297">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="fde50-298">`[ContainerSize <Int32?>]`: Funktions behållaens storlek.</span><span class="sxs-lookup"><span data-stu-id="fde50-298">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="fde50-299">`[DailyMemoryTimeQuota <Int32?>]`: Högsta tillåtna mängd minne – tids kvot (gäller endast dynamiska program).</span><span class="sxs-lookup"><span data-stu-id="fde50-299">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="fde50-300">`[Enabled <Boolean?>]`: <code>true</code> om appen är aktive rad, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fde50-300">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="fde50-301">Om du anger det här värdet till false inaktive ras programmet (tar programmet offline).</span><span class="sxs-lookup"><span data-stu-id="fde50-301">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="fde50-302">`[HostNameSslState <IHostNameSslState[]>]`: Hostname för SSL-tillstånd används för att hantera SSL-bindningar för programmets värdnamn.</span><span class="sxs-lookup"><span data-stu-id="fde50-302">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="fde50-303">`[HostType <HostType?>]`: Anger om värd namnet är en standard-eller databas värd.</span><span class="sxs-lookup"><span data-stu-id="fde50-303">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="fde50-304">`[Name <String>]`Namn.</span><span class="sxs-lookup"><span data-stu-id="fde50-304">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="fde50-305">`[SslState <SslState?>]`: SSL-typ.</span><span class="sxs-lookup"><span data-stu-id="fde50-305">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="fde50-306">`[Thumbprint <String>]`: Tumavtryck för SSL-certifikat.</span><span class="sxs-lookup"><span data-stu-id="fde50-306">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="fde50-307">`[ToUpdate <Boolean?>]`: Angett för <code>true</code> att uppdatera befintligt värdnamn.</span><span class="sxs-lookup"><span data-stu-id="fde50-307">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="fde50-308">`[VirtualIP <String>]`: Virtuell IP-adress som tilldelats värd namnet om IP-baserad SSL är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="fde50-308">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="fde50-309">`[HostNamesDisabled <Boolean?>]`: <code>true</code> så här inaktiverar du de offentliga värdarna för appen, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fde50-309">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="fde50-310">Om <code>true</code> programmet endast är tillgängligt via API Management process.</span><span class="sxs-lookup"><span data-stu-id="fde50-310">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="fde50-311">`[HostingEnvironmentProfileId <String>]`: Resurs-ID för App Service Environment.</span><span class="sxs-lookup"><span data-stu-id="fde50-311">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="fde50-312">`[HttpsOnly <Boolean?>]`: HttpsOnly: konfigurerar en webbplats för att acceptera endast HTTPS-begäranden.</span><span class="sxs-lookup"><span data-stu-id="fde50-312">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="fde50-313">Problem vid omdirigering för HTTP-begäranden</span><span class="sxs-lookup"><span data-stu-id="fde50-313">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="fde50-314">`[HyperV <Boolean?>]`: Hyper-V Sand låda.</span><span class="sxs-lookup"><span data-stu-id="fde50-314">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="fde50-315">`[IdentityType <ManagedServiceIdentityType?>]`: Typen av hanterad tjänst identitet.</span><span class="sxs-lookup"><span data-stu-id="fde50-315">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="fde50-316">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Listan med användare tilldelade identiteter associerade med resursen.</span><span class="sxs-lookup"><span data-stu-id="fde50-316">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="fde50-317">Nyckelorden för användar identitets ord lista kommer att vara resurs-ID: n i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="fde50-317">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="fde50-318">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.</span><span class="sxs-lookup"><span data-stu-id="fde50-318">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="fde50-319">`[IsXenon <Boolean?>]`: Överflödig: Sand låda för Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="fde50-319">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="fde50-320">`[RedundancyMode <RedundancyMode?>]`: Läget för webbplats redundans</span><span class="sxs-lookup"><span data-stu-id="fde50-320">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="fde50-321">`[Reserved <Boolean?>]`: <code>true</code> om det reserveras; annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fde50-321">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="fde50-322">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> stoppa SCM (kudu)-webbplatsen när appen stoppas, annars <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fde50-322">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="fde50-323">Standardvärdet är <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="fde50-323">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="fde50-324">`[ServerFarmId <String>]`: Resurs-ID för den associerade App Service-planen, formaterad som: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span><span class="sxs-lookup"><span data-stu-id="fde50-324">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="fde50-325">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fde50-325">RELATED LINKS</span></span>

