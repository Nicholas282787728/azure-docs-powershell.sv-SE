---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/start-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Start-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Start-AzFunctionApp.md
ms.openlocfilehash: c5c5fd14f61be2526c62335b9f6ed33719846a12
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100973"
---
# Start-AzFunctionApp

## Sammanfattning
Startar en Function-app.

## FRÅGESYNTAXEN

### StartByName (standard)
```
Start-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Start-AzFunctionApp -InputObject <ISite> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Startar en Function-app.

## BESKRIVS

### Exempel 1: Hämta en funktion app genom att namnge och starta den.
```powershell
PS C:\> Get-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName | Start-AzFunctionApp
```

Det här kommandot får en funktion-app efter namn och startar det.

### Exempel 2: starta en funktion app efter namn.
```powershell
PS C:\> Start-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName
```

Det här kommandot startar en Function-app efter namn.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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

### -InputObject
För att konstruera kan du läsa avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.

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

### -Namn
Namnet på funktions programmet.

```yaml
Type: System.String
Parameter Sets: StartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returnerar sant när kommandot fungerar.

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

### -ResourceGroupName


```yaml
Type: System.String
Parameter Sets: StartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ID för Azure-prenumeration.

```yaml
Type: System.String
Parameter Sets: StartByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

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

### -WhatIf
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### Microsoft. Azure. PowerShell. cmdletar. functions. Models. Api20190801. ISite

## VÄRDEN

### System. Boolean

## ANMÄRKNINGAR

ALIAS

KOMPLEXA PARAMETER EGENSKAPER

Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan. Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.


INPUTOBJECT <ISite> : 
  - `Location <String>`: Resurs plats.
  - `CloningInfoSourceWebAppId <String>`: Käll programmets ID för ARM-resurs. App-resurs-ID är/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} för produktions platser och/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} för andra platser.
  - `[Kind <String>]`: Typ av resurs.
  - `[Tag <IResourceTags>]`: Resursfiler.
    - `[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.
  - `[ClientAffinityEnabled <Boolean?>]`: <code>true</code> så här aktiverar du klient tillhörighet <code>false</code> för att sluta skicka cookie-cookies, som dirigerar klienter i samma session till samma instans. Standard är <code>true</code> .
  - `[ClientCertEnabled <Boolean?>]`: <code>true</code> så här aktiverar du klientautentisering för klient certifikat (gemensam TLS-verifikation), annars <code>false</code> . Standard är <code>false</code> .
  - `[ClientCertExclusionPath <String>]`: meddelandeautentisering-avgränsade sökvägar för klient certifikat
  - `[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Program inställning åsidosätter för klonad app. Om det här alternativet anges åsidosätter dessa inställningar de inställningar som klonas från käll programmet. Annars sparas program inställningar från käll programmet.
    - `[(Any) <String>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.
  - `[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> för att klona anpassade värdnamn från käll programmet, annars <code>false</code> .
  - `[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> för att klona käll kontrollen från käll programmet, annars <code>false</code> .
  - `[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> för att konfigurera belastnings utjämning för käll-och mål programmet.
  - `[CloningInfoCorrelationId <String>]`: Korrelations-ID för klonings åtgärden. Detta ID bevarar flera klonings operationer tillsammans för att använda samma ögonblicks bild.
  - `[CloningInfoHostingEnvironment <String>]`: App Service Environment.
  - `[CloningInfoOverwrite <Boolean?>]`: <code>true</code> för att skriva över mål programmet, annars, <code>false</code> .
  - `[CloningInfoSourceWebAppLocation <String>]`: Käll appens plats, t. ex.
  - `[CloningInfoTrafficManagerProfileId <String>]`: ID för den Traffic Manager-profil som ska användas, om den finns. Resurs-ID för Traffic Manager har formen/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.
  - `[CloningInfoTrafficManagerProfileName <String>]`: Namnet på Traffic Manager-profilen som ska skapas. Detta krävs endast om Traffic Manager-profilen inte redan finns.
  - `[Config <ISiteConfig>]`: Programmets konfiguration.
    - `IsPushEnabled <Boolean>`: Hämtar eller anger en flagga som anger om push-slutpunkten är aktive rad.
    - `[ActionMinProcessExecutionTime <String>]`: Minsta tid då processen måste utföras innan åtgärden utförs
    - `[ActionType <AutoHealActionType?>]`: Fördefinierad åtgärd som ska vidtas.
    - `[AlwaysOn <Boolean?>]`: <code>true</code> om Always On är aktiverat, annars <code>false</code> .
    - `[ApiDefinitionUrl <String>]`: API-definitionen URL.
    - `[ApiManagementConfigId <String>]`: APIM-Api-ID.
    - `[AppCommandLine <String>]`: Programmets kommando rad för start.
    - `[AppSetting <INameValuePair[]>]`: Program inställningar.
      - `[Name <String>]`: Parets namn.
      - `[Value <String>]`: Paret.
    - `[AutoHealEnabled <Boolean?>]`: <code>true</code> om Auto läka är aktiverat, annars <code>false</code> .
    - `[AutoSwapSlotName <String>]`: Byt plats namn automatiskt.
    - `[ConnectionString <IConnStringInfo[]>]`: Anslutnings strängar.
      - `[ConnectionString <String>]`: Anslutnings sträng värde.
      - `[Name <String>]`: Anslutnings strängens namn.
      - `[Type <ConnectionStringType?>]`: Typ av databas.
    - `[CorAllowedOrigin <String[]>]`: Hämtar eller anger listan över ursprung som ska tillåtas att ringa kors ursprung (till exempel: http://example.com:12345) . Använd "*" för att tillåta alla.
    - `[CorSupportCredentials <Boolean?>]`: Hämtar eller anger om CORS-begäranden med autentiseringsuppgifter är tillåtna. Se         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         för mer information.
    - `[CustomActionExe <String>]`: Den körbara filen körs.
    - `[CustomActionParameter <String>]`: Parametrar för den körbara filen.
    - `[DefaultDocument <String[]>]`: Standard dokument.
    - `[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> om detaljerad fel loggning är aktive rad, annars <code>false</code> .
    - `[DocumentRoot <String>]`: Dokument rot.
    - `[DynamicTagsJson <String>]`: Hämtar eller anger en JSON-sträng som innehåller en lista över dynamiska taggar som ska utvärderas från användar anspråk i push-registrerings slut punkten.
    - `[ExperimentRampUpRule <IRampUpRule[]>]`: Lista över regler för ramp up.
      - `[ActionHostName <String>]`: Värd namnet för en plats där trafiken ska omdirigeras om det har beslut ATS. Namn@example.com. myapp-stage.azurewebsites.net.
      - `[ChangeDecisionCallbackUrl <String>]`: Den anpassade besluts algoritmen kan tillhandahållas i TiPCallback som webb adress (URL) kan anges. Se TiPCallback webbplats tillägg för stödjer och kontrakt.         https://www.siteextensions.net/packages/TiPCallback/
      - `[ChangeIntervalInMinute <Int32?>]`: Anger intervall i minuter för att utvärdera ReroutePercentage.
      - `[ChangeStep <Double?>]`: I scenario för automatisk ramp kan du lägga till/ta bort från <code>ReroutePercentage</code> tills det når \n <code>MinReroutePercentage</code> eller         <code>MaxReroutePercentage</code> . Webbplats mått kontrol leras var N minuter som anges i <code>ChangeIntervalInMinutes</code> .\nCustom besluts algoritm kan tillhandahållas i TiPCallback webbplats tillägg som URL: en kan anges i <code>ChangeDecisionCallbackUrl</code> .
      - `[MaxReroutePercentage <Double?>]`: Anger övre gräns nedanför vilken ReroutePercentage förblir.
      - `[MinReroutePercentage <Double?>]`: Anger nedre gräns ovanför vilken ReroutePercentage blir.
      - `[Name <String>]`: Namnet på regeln. Det rekommenderade namnet är att peka på den plats där trafiken tas emot i experimentet.
      - `[ReroutePercentage <Double?>]`: Procent andel av trafiken som kommer att omdirigeras till <code>ActionHostName</code> .
    - `[FtpsState <FtpsState?>]`: FTP-FTPS
    - `[HandlerMapping <IHandlerMapping[]>]`: Hanterarmappning.
      - `[Argument <String>]`: Kommando rads argument som ska överföras till skript processorn.
      - `[Extension <String>]`: Förfrågningar med den här tillägget hanteras med det angivna FastCGI-programmet.
      - `[ScriptProcessor <String>]`: Den absoluta sökvägen till FastCGI-programmet.
    - `[HealthCheckPath <String>]`: Hälso kontroll Sök väg
    - `[Http20Enabled <Boolean?>]`: Http20Enabled: konfigurerar en webbplats för att tillåta klienter att ansluta via http 2.0
    - `[HttpLoggingEnabled <Boolean?>]`: <code>true</code> om HTTP-loggning är aktiverat, annars <code>false</code> .
    - `[IPSecurityRestriction <IIPSecurityRestriction[]>]`: Begränsningar för IP-säkerhet för huvud.
      - `[Action <String>]`: Tillåt eller neka åtkomst för detta IP-intervall.
      - `[Description <String>]`: Beskrivning för regel för IP-begränsning.
      - `[IPAddress <String>]`: IP-adress säkerhets begränsningen är giltig för.         Den kan vara i form av en ren IPv4-adress (obligatoriskt nätmask-egenskap) eller CIDR-notering, till exempel IPv4/mask (inledande bit träff). Egenskapen nätmask måste anges.
      - `[Name <String>]`: Namn på regel för IP-begränsning.
      - `[Priority <Int32?>]`: Prioritet för IP-begränsning regeln.
      - `[SubnetMask <String>]`: Nät masken för intervallet med IP-adresser begränsningen är giltig för.
      - `[SubnetTrafficTag <Int32?>]`: (intern) kod för nät trafik
      - `[Tag <IPFilterTag?>]`: Definierar vad det här IP-filtret ska användas till. Detta är till för att stödja IP-filtrering på proxyservrar.
      - `[VnetSubnetResourceId <String>]`: ID för virtuell nätverks resurs
      - `[VnetTrafficTag <Int32?>]`: (intern) tagg för VNet-trafik
    - `[JavaContainer <String>]`: Java-behållare.
    - `[JavaContainerVersion <String>]`: Java-container version.
    - `[JavaVersion <String>]`: Java-version.
    - `[LimitMaxDiskSizeInMb <Int64?>]`: Maximal mängd disk storlek i MB.
    - `[LimitMaxMemoryInMb <Int64?>]`: Högsta tillåtna minnes användning i MB.
    - `[LimitMaxPercentageCpu <Double?>]`: Högsta tillåtna processor användnings procent.
    - `[LinuxFxVersion <String>]`: Linux program ramverk och-version
    - `[LoadBalancing <SiteLoadBalancing?>]`: Utjämning av webbplats belastning.
    - `[LocalMySqlEnabled <Boolean?>]`: <code>true</code> för att aktivera lokal MySQL; <code>false</code>
    - `[LogsDirectorySizeLimit <Int32?>]`: HTTP-loggningens storleks gräns.
    - `[MachineKeyDecryption <String>]`: Algoritm som används för dekryptering.
    - `[MachineKeyDecryptionKey <String>]`: Dekrypteringsnyckel.
    - `[MachineKeyValidation <String>]`: MachineKey-verifiering.
    - `[MachineKeyValidationKey <String>]`: Verifierings tangenten.
    - `[ManagedPipelineMode <ManagedPipelineMode?>]`: Hanterat pipeline-läge.
    - `[ManagedServiceIdentityId <Int32?>]`: ID för hanterad tjänst identitet
    - `[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: konfigurerar den minsta versionen av TLS som krävs för SSL-begäranden
    - `[NetFrameworkVersion <String>]`: .NET Framework-version.
    - `[NodeVersion <String>]`: Version av Node.js.
    - `[NumberOfWorker <Int32?>]`: Antal anställda.
    - `[PhpVersion <String>]`: Version av PHP.
    - `[PowerShellVersion <String>]`: Version av PowerShell.
    - `[PreWarmedInstanceCount <Int32?>]`: Antal invärmade instanser.         Den här inställningen gäller endast för förbrukning och elastiska abonnemang
    - `[PublishingUsername <String>]`: Publicera användar namn.
    - `[PushKind <String>]`: Typ av resurs.
    - `[PythonVersion <String>]`: Version av python.
    - `[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> om fjärrfelsökning är aktive rad, annars <code>false</code> .
    - `[RemoteDebuggingVersion <String>]`: Remote debug-version.
    - `[RequestCount <Int32?>]`: Antal förfrågningar.
    - `[RequestTimeInterval <String>]`: Tidsintervall.
    - `[RequestTracingEnabled <Boolean?>]`: <code>true</code> om spårning för förfrågningar är aktiverat, annars <code>false</code> .
    - `[RequestTracingExpirationTime <DateTime?>]`: Spårnings tiden förfaller.
    - `[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-säkerhetsrestriktioner för SCM.
    - `[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP-säkerhetsrestriktioner för SCM för att använda main.
    - `[ScmType <ScmType?>]`: SCM-typ.
    - `[SlowRequestCount <Int32?>]`: Antal förfrågningar.
    - `[SlowRequestTimeInterval <String>]`: Tidsintervall.
    - `[SlowRequestTimeTaken <String>]`: Åtgången tid.
    - `[TagWhitelistJson <String>]`: Hämtar eller anger en JSON-sträng som innehåller en lista med taggar som är whitelisted för användning av push-registrerings slut punkten.
    - `[TagsRequiringAuth <String>]`: Hämtar eller anger en JSON-sträng som innehåller en lista med taggar som kräver att användarautentisering används i push-registrerings slut punkten.         Taggar kan bestå av alfanumeriska tecken och följande: "_", "@", "#", ".", ":", "-".         Verifiering ska utföras på PushRequestHandler.
    - `[TracingOption <String>]`: Spårnings alternativ.
    - `[TriggerPrivateBytesInKb <Int32?>]`: En regel baserad på privata byte.
    - `[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: En regel baserad på status koder.
      - `[Count <Int32?>]`: Antal förfrågningar.
      - `[Status <Int32?>]`: HTTP-statuskod.
      - `[SubStatus <Int32?>]`: Under status för begäran.
      - `[TimeInterval <String>]`: Tidsintervall.
      - `[Win32Status <Int32?>]`: Win32-felkod.
    - `[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> för att använda 32-bitars arbets process, annars <code>false</code> .
    - `[VirtualApplication <IVirtualApplication[]>]`: Virtuella program.
      - `[PhysicalPath <String>]`: Fysisk sökväg.
      - `[PreloadEnabled <Boolean?>]`: <code>true</code> om för inläsning är aktiverat, annars <code>false</code> .
      - `[VirtualDirectory <IVirtualDirectory[]>]`: Virtuella kataloger för virtuella program.
        - `[PhysicalPath <String>]`: Fysisk sökväg.
        - `[VirtualPath <String>]`: Sökväg till virtuellt program.
      - `[VirtualPath <String>]`: Virtuell sökväg.
    - `[VnetName <String>]`: Virtuellt nätverks namn.
    - `[WebSocketsEnabled <Boolean?>]`: <code>true</code> om WebSocket är aktiverat, annars, <code>false</code> .
    - `[WindowsFxVersion <String>]`: Xenon program ramverk och-version
    - `[XManagedServiceIdentityId <Int32?>]`: Explicit hanterat identitets-ID
  - `[ContainerSize <Int32?>]`: Funktions behållaens storlek.
  - `[DailyMemoryTimeQuota <Int32?>]`: Högsta tillåtna mängd minne – tids kvot (gäller endast dynamiska program).
  - `[Enabled <Boolean?>]`: <code>true</code> om appen är aktive rad, annars <code>false</code> . Om du anger det här värdet till false inaktive ras programmet (tar programmet offline).
  - `[HostNameSslState <IHostNameSslState[]>]`: Hostname för SSL-tillstånd används för att hantera SSL-bindningar för programmets värdnamn.
    - `[HostType <HostType?>]`: Anger om värd namnet är en standard-eller databas värd.
    - `[Name <String>]`Namn.
    - `[SslState <SslState?>]`: SSL-typ.
    - `[Thumbprint <String>]`: Tumavtryck för SSL-certifikat.
    - `[ToUpdate <Boolean?>]`: Angett för <code>true</code> att uppdatera befintligt värdnamn.
    - `[VirtualIP <String>]`: Virtuell IP-adress som tilldelats värd namnet om IP-baserad SSL är aktiverat.
  - `[HostNamesDisabled <Boolean?>]`: <code>true</code> så här inaktiverar du de offentliga värdarna för appen, annars <code>false</code> .          Om <code>true</code> programmet endast är tillgängligt via API Management process.
  - `[HostingEnvironmentProfileId <String>]`: Resurs-ID för App Service Environment.
  - `[HttpsOnly <Boolean?>]`: HttpsOnly: konfigurerar en webbplats för att acceptera endast HTTPS-begäranden. Problem vid omdirigering för HTTP-begäranden
  - `[HyperV <Boolean?>]`: Hyper-V Sand låda.
  - `[IdentityType <ManagedServiceIdentityType?>]`: Typen av hanterad tjänst identitet.
  - `[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Listan med användare tilldelade identiteter associerade med resursen. Nyckelorden för användar identitets ord lista kommer att vara resurs-ID: n i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}
    - `[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Detta indikerar att en egenskap kan läggas till i det här objektet.
  - `[IsXenon <Boolean?>]`: Överflödig: Sand låda för Hyper-V.
  - `[RedundancyMode <RedundancyMode?>]`: Läget för webbplats redundans
  - `[Reserved <Boolean?>]`: <code>true</code> om det reserveras; annars <code>false</code> .
  - `[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> stoppa SCM (kudu)-webbplatsen när appen stoppas, annars <code>false</code> . Standardvärdet är <code>false</code> .
  - `[ServerFarmId <String>]`: Resurs-ID för den associerade App Service-planen, formaterad som: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".

## RELATERADE LÄNKAR

