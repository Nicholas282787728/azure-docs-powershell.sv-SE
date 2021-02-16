---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppSetting.md
ms.openlocfilehash: 4255940b9cf17420fe0b522d81c6a974e9cf9324
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100222462"
---
# Update-AzFunctionAppSetting

## SYNOPSIS
Lägger till eller uppdaterar appinställningar i en funktionsapp.

## SYNTAX

### ByName (standard)
```
Update-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> -AppSetting <Hashtable>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Update-AzFunctionAppSetting -AppSetting <Hashtable> -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## BESKRIVNING
Lägger till eller uppdaterar appinställningar i en funktionsapp.

## EXEMPEL

### Exempel 1: Lägga till en ny appinställning i en funktionsapp.
```powershell
PS C:\> Update-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName -AppSetting @{"Name1" = "Value1"}
```

Med det här kommandot läggs en ny appinställning till i en funktionsapp.

## PARAMETERS

### -AppSetting
Hashtabell med nycklar och värden beskriver appinställningarna som ska läggas till eller uppdateras i funktionsappen.
Till exempel: @{"myappsetting"="123"}

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

### -DefaultProfile


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

### -Force
Tvingar cmdleten att uppdatera funktionsappens inställning utan att behöva bekräfta.

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

### -InputObject
Skapa genom att gå till avsnittet NOTES för INPUTOBJECT-egenskaper och skapa en hash-tabell.

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

### -Name
Namnet på funktionsappen.

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

### -ResourceGroupName
Namn på resursgruppen som resursen tillhör.

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

### -SubscriptionId
Azure-prenumerations-ID.

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

### -Bekräfta
Frågar dig om bekräftelse innan du kör cmdleten.

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
Visar vad som skulle hända om cmdleten körs.
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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Microsoft.Azure.PowerShell.cmdlets.Functions.Models.API20190801.ISite

## UTDATA

### Microsoft.Azure.PowerShell.cmdlets.Functions.Models.Api20190801.IStringDictionary

## ANTECKNINGAR

ALIAS

KOMPLEXA PARAMETEREGENSKAPER

Skapa de parametrar som beskrivs nedan genom att skapa en hash-tabell som innehåller rätt egenskaper. Om du vill ha information om hash-tabeller kör du Get-Help about_Hash_Tables.


INPUTOBJECT: <ISite> 
  - `Location <String>`: Resursplats.
  - `CloningInfoSourceWebAppId <String>`: ARM resurs-ID för källprogrammet. Appresurs-ID är formuläret /prenumerationer/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} för produktionsplatser och /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slot/{slotName} för andra platser.
  - `[Kind <String>]`: Typ av resurs.
  - `[Tag <IResourceTags>]`: Resurstaggar.
    - `[(Any) <String>]`: Detta anger att alla egenskapen kan läggas till i objektet.
  - `[ClientAffinityEnabled <Boolean?>]`: om du vill aktivera klienttillhörighet, sluta skicka <code>true</code> sessionstillhörigheter till cookies, vilket dirigerar klientförfrågningar i <code>false</code> samma session till samma instans. Standardvärdet är <code>true</code> .
  - `[ClientCertEnabled <Boolean?>]`: <code>true</code> om du vill aktivera autentisering med klientcertifikat (TLS-gemensam autentisering), <code>false</code> annars. Standardvärdet är <code>false</code> .
  - `[ClientCertExclusionPath <String>]`: kommaavgränsade undantagssökvägar för klientcertifikatautentisering
  - `[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Programinställningar åsidosätter klonade appar. Om den anges åsidosätter de här inställningarna inställningarna klonade från källappen. Annars behålls programinställningarna från källappen.
    - `[(Any) <String>]`: Detta anger att alla egenskapen kan läggas till i objektet.
  - `[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> om du vill klona egna värdnamn från källappen. <code>false</code>
  - `[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> om du vill klona källkontrollen från källappen. <code>false</code>
  - `[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> om du vill konfigurera belastningsutjämning för käll- och målappen.
  - `[CloningInfoCorrelationId <String>]`: Korrelations-ID för operation av operation. Det här ID:t kan användas för att hantera flera objekt samtidigt för att kunna använda samma ögonblicksbild.
  - `[CloningInfoHostingEnvironment <String>]`: Apptjänstmiljö.
  - `[CloningInfoOverwrite <Boolean?>]`: <code>true</code> om du vill skriva över målappen, <code>false</code> annars.
  - `[CloningInfoSourceWebAppLocation <String>]`: Platsen för källappen, t.ex. Västra USA eller Norra Europa
  - `[CloningInfoTrafficManagerProfileId <String>]`: ARM resurs-ID för profilen i Trafikhanteraren som ska användas, om den finns. Resurs-ID för Trafikhanteraren är formuläret /prenumerationer/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.
  - `[CloningInfoTrafficManagerProfileName <String>]`: Namn på profilen i Trafikhanteraren som ska skapas. Det här behövs bara om Traffic Manager-profilen inte redan finns.
  - `[Config <ISiteConfig>]`: Konfiguration av appen.
    - `IsPushEnabled <Boolean>`: Hämtar eller anger en flagga som anger om Push-slutpunkten är aktiverad.
    - `[ActionMinProcessExecutionTime <String>]`: Den minsta tid som processen måste köras innan åtgärden vidtas
    - `[ActionType <AutoHealActionType?>]`: Fördefinierad åtgärd som ska vidtas.
    - `[AlwaysOn <Boolean?>]`: <code>true</code> om Alltid på är aktiverat, <code>false</code> annars.
    - `[ApiDefinitionUrl <String>]`: URL:en för API-definitionen.
    - `[ApiManagementConfigId <String>]`: APIM-Api Identifierare.
    - `[AppCommandLine <String>]`: App-kommandoraden för att starta.
    - `[AppSetting <INameValuePair[]>]`: Programinställningar.
      - `[Name <String>]`: Namn på par.
      - `[Value <String>]`: Värde för par.
    - `[AutoHealEnabled <Boolean?>]`: <code>true</code> om Automatisk den här funktionen är aktiverad, <code>false</code> annars.
    - `[AutoSwapSlotName <String>]`: Namn på plats för automatiskt byte.
    - `[ConnectionString <IConnStringInfo[]>]`: Anslutningssträngar.
      - `[ConnectionString <String>]`: Värdet för anslutningssträngen.
      - `[Name <String>]`: Namn på anslutningssträng.
      - `[Type <ConnectionStringType?>]`: Typ av databas.
    - `[CorAllowedOrigin <String[]>]`: Hämtar eller anger listan över ursprung som ska kunna ringa korssprungssamtal (till exempel: http://example.com:12345) . Använd "*" för att tillåta alla.
    - `[CorSupportCredentials <Boolean?>]`: Hämtar eller anger om KORS-begäranden med autentiseringsuppgifter ska tillåtas. Mer         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         information finns i
    - `[CustomActionExe <String>]`: Körbar.
    - `[CustomActionParameter <String>]`: Parametrar för den körbara filen.
    - `[DefaultDocument <String[]>]`: Standarddokument.
    - `[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> om detaljerad felloggning är aktiverad. <code>false</code>
    - `[DocumentRoot <String>]`: Dokumentroten.
    - `[DynamicTagsJson <String>]`: Hämtar eller anger en JSON-sträng som innehåller en lista med dynamiska taggar som ska utvärderas från användarens anspråk i push-registreringsslutpunkten.
    - `[ExperimentRampUpRule <IRampUpRule[]>]`: Lista över upprammningsregler.
      - `[ActionHostName <String>]`: Värdnamn för en plats som trafiken omdirigeras till om den bestäms till. T.ex. myapp-stage.azurewebsites.net.
      - `[ChangeDecisionCallbackUrl <String>]`: Anpassad beslutsalgoritm kan tillhandahållas i TiPCallback-webbplatstillägget vilken URL som kan anges. Se TiPCallback-webbplatstillägget för de skabbiga kontrakten.         https://www.siteextensions.net/packages/TiPCallback/
      - `[ChangeIntervalInMinute <Int32?>]`: Anger intervallet i minuter för att omvärdera OmroutePercentage.
      - `[ChangeStep <Double?>]`: I scenariot Auto ramp up är det här steget för att lägga till/ta bort <code>ReroutePercentage</code> från tills det når \n <code>MinReroutePercentage</code> eller         <code>MaxReroutePercentage</code> . Webbplatsmått kontrolleras var N:e minut som anges i .\nCustom-beslutsalgoritmen kan anges i TiPCallback-webbplatstillägget som URL-adressen kan <code>ChangeIntervalInMinutes</code> anges <code>ChangeDecisionCallbackUrl</code> i.
      - `[MaxReroutePercentage <Double?>]`: Anger den övre gränsen under vilken ReroutePercentage stannar.
      - `[MinReroutePercentage <Double?>]`: Anger undre gräns ovanför vilken ReroutePercentage ska stanna.
      - `[Name <String>]`: Namnet på routningsregeln. Det rekommenderade namnet är att peka på den plats som tar emot trafiken i experimentet.
      - `[ReroutePercentage <Double?>]`: Procentandel av trafiken som kommer att dirigeras om <code>ActionHostName</code> till.
    - `[FtpsState <FtpsState?>]`: Status för FTP-/FTPS-tjänsten
    - `[HandlerMapping <IHandlerMapping[]>]`: Handler-mappningar.
      - `[Argument <String>]`: Kommandoradsargument som ska skickas till skriptprocessorn.
      - `[Extension <String>]`: Begäranden med det här tillägget hanteras med det angivna FastCGI-programmet.
      - `[ScriptProcessor <String>]`: Den absoluta sökvägen till FastCGI-programmet.
    - `[HealthCheckPath <String>]`: Sökväg för hälsokontroll
    - `[Http20Enabled <Boolean?>]`: Http20Enabled: konfigurerar en webbplats så att klienter kan ansluta via http2.0
    - `[HttpLoggingEnabled <Boolean?>]`: <code>true</code> om HTTP-loggning är aktiverat, <code>false</code> annars.
    - `[IPSecurityRestriction <IIPSecurityRestriction[]>]`: Ip-säkerhetsbegränsningar för huvudsidan.
      - `[Action <String>]`: Tillåt eller neka åtkomst för det här IP-intervallet.
      - `[Description <String>]`: Beskrivning av ip-begränsningsregel.
      - `[IPAddress <String>]`: IP-adress som säkerhetsbegränsningen gäller för.         Det kan vara i form av endast ipv4-adress (obligatorisk undernätmaskegenskap) eller CIDR-notation som ipv4/mask (inledande bitmatchning). För CIDR får inte egenskapen SubnetMask anges.
      - `[Name <String>]`: Namn på ip-begränsningsregel.
      - `[Priority <Int32?>]`: Prioritet för ip-begränsningsregeln.
      - `[SubnetMask <String>]`: Undernätsmask för det intervall av IP-adresser som begränsningen gäller för.
      - `[SubnetTrafficTag <Int32?>]`: (internt) trafiktagg för undernät
      - `[Tag <IPFilterTag?>]`: Definierar vad ip-filtret ska användas till. Detta är för att stödja IP-filtrering på proxy.
      - `[VnetSubnetResourceId <String>]`: Virtuellt nätverksresurs-ID
      - `[VnetTrafficTag <Int32?>]`: (intern) Vnet-trafiktagg
    - `[JavaContainer <String>]`: Java-behållare.
    - `[JavaContainerVersion <String>]`: Java-behållarversion.
    - `[JavaVersion <String>]`: Java-version.
    - `[LimitMaxDiskSizeInMb <Int64?>]`: Maximal tillåten användning av diskstorlek i MB.
    - `[LimitMaxMemoryInMb <Int64?>]`: Maximal tillåten minnesanvändning i MB.
    - `[LimitMaxPercentageCpu <Double?>]`: Maximal tillåten CPU-användning i procent.
    - `[LinuxFxVersion <String>]`: Linux App Framework och version
    - `[LoadBalancing <SiteLoadBalancing?>]`: Belastningsutjämning för webbplatser.
    - `[LocalMySqlEnabled <Boolean?>]`: <code>true</code> om du vill aktivera lokal MySQL, <code>false</code> annars.
    - `[LogsDirectorySizeLimit <Int32?>]`: HTTP loggar storleksgränsen för katalogen.
    - `[MachineKeyDecryption <String>]`: Algoritm som används för dekryptering.
    - `[MachineKeyDecryptionKey <String>]`: Dekrypteringstangent.
    - `[MachineKeyValidation <String>]`: Maskinnyckelverifiering.
    - `[MachineKeyValidationKey <String>]`: Verifieringsnyckel.
    - `[ManagedPipelineMode <ManagedPipelineMode?>]`: Läget Hanterad rörledning.
    - `[ManagedServiceIdentityId <Int32?>]`: Identitets-ID för hanterad tjänst
    - `[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: konfigurerar den lägsta versionen av TLS som krävs för SSL-begäranden
    - `[NetFrameworkVersion <String>]`: .NET Framework-versionen.
    - `[NodeVersion <String>]`: Version av Node.js.
    - `[NumberOfWorker <Int32?>]`: Antal medarbetare.
    - `[PhpVersion <String>]`: Version av PHP.
    - `[PowerShellVersion <String>]`: Version av PowerShell.
    - `[PreWarmedInstanceCount <Int32?>]`: Antal förvarningsinstanser.         Den här inställningen gäller endast för förbruknings- och flexibelt-abonnemang
    - `[PublishingUsername <String>]`: Publicera användarnamn.
    - `[PushKind <String>]`: Typ av resurs.
    - `[PythonVersion <String>]`: Version av Python.
    - `[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> om fjärrfelsökning är aktiverat, <code>false</code> annars.
    - `[RemoteDebuggingVersion <String>]`: Fjärrfelsökningsversion.
    - `[RequestCount <Int32?>]`: Antal begäran.
    - `[RequestTimeInterval <String>]`: Tidsintervall.
    - `[RequestTracingEnabled <Boolean?>]`: <code>true</code> om spårning av begäran är aktiverat, <code>false</code> annars.
    - `[RequestTracingExpirationTime <DateTime?>]`: Begär förfallodatum för spårning.
    - `[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP-säkerhetsbegränsningar för scm.
    - `[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP-säkerhetsbegränsningar för att SCM ska använda huvud.
    - `[ScmType <ScmType?>]`: SCM-typ.
    - `[SlowRequestCount <Int32?>]`: Antal begäran.
    - `[SlowRequestTimeInterval <String>]`: Tidsintervall.
    - `[SlowRequestTimeTaken <String>]`: Tidstagna.
    - `[TagWhitelistJson <String>]`: Hämtar eller anger en JSON-sträng som innehåller en lista med taggar som har vitlistats för användning av push-registreringsslutpunkten.
    - `[TagsRequiringAuth <String>]`: Hämtar eller anger en JSON-sträng som innehåller en lista med taggar som kräver att användarautentisering används i push-registreringsslutpunkten.         Taggar kan bestå av alfanumeriska tecken och följande: '_', '@', '#', '.', ':', '-'.         Verifiering ska utföras hos PushRequestHandler.
    - `[TracingOption <String>]`: Spårningsalternativ.
    - `[TriggerPrivateBytesInKb <Int32?>]`: En regel som baseras på privata byte.
    - `[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: En regel som baseras på statuskoder.
      - `[Count <Int32?>]`: Antal begäran.
      - `[Status <Int32?>]`: HTTP-statuskod.
      - `[SubStatus <Int32?>]`: Begär understatus.
      - `[TimeInterval <String>]`: Tidsintervall.
      - `[Win32Status <Int32?>]`: Win32-felkod.
    - `[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> om du vill använda 32-bitars arbetsprocess, <code>false</code> annars.
    - `[VirtualApplication <IVirtualApplication[]>]`: Virtuella program.
      - `[PhysicalPath <String>]`: Fysisk sökväg.
      - `[PreloadEnabled <Boolean?>]`: <code>true</code> om förinläsning är aktiverat, <code>false</code> annars.
      - `[VirtualDirectory <IVirtualDirectory[]>]`: Virtuella kataloger för virtuell applikation.
        - `[PhysicalPath <String>]`: Fysisk sökväg.
        - `[VirtualPath <String>]`: Sökväg till virtuellt program.
      - `[VirtualPath <String>]`: Virtuell sökväg.
    - `[VnetName <String>]`: Namn på virtuellt nätverk.
    - `[WebSocketsEnabled <Boolean?>]`: <code>true</code> om WebSocket är aktiverat, <code>false</code> annars.
    - `[WindowsFxVersion <String>]`: Xenon App Framework och version
    - `[XManagedServiceIdentityId <Int32?>]`: Identitets-ID för explicit hanterad tjänst
  - `[ContainerSize <Int32?>]`: Storlek på funktionsbehållaren.
  - `[DailyMemoryTimeQuota <Int32?>]`: Maximal tillåten daglig minneskvot (gäller endast dynamiska appar).
  - `[Enabled <Boolean?>]`: <code>true</code> om appen är aktiverad, <code>false</code> annars. Om du anger det här värdet falskt inaktiveras appen (appen inaktiveras offline).
  - `[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL-tillstånd används för att hantera SSL-bindningarna för appens värdnamn.
    - `[HostType <HostType?>]`: Anger om värdnamnet är standard- eller lagringsplatsvärdnamn.
    - `[Name <String>]`: Hostname.
    - `[SslState <SslState?>]`: SSL-typ.
    - `[Thumbprint <String>]`: SSL-certifikat tumavtryck.
    - `[ToUpdate <Boolean?>]`: Ange att <code>true</code> uppdatera befintligt värdnamn.
    - `[VirtualIP <String>]`: Virtuell IP-adress tilldelad till värdnamnet om IP-baserat SSL är aktiverat.
  - `[HostNamesDisabled <Boolean?>]`: om du vill inaktivera appens offentliga <code>true</code> värdnamn, <code>false</code> annars.          Om <code>true</code> programmet bara är åtkomligt via API-hanteringsprocessen.
  - `[HostingEnvironmentProfileId <String>]`: Resurs-ID för apptjänstmiljön.
  - `[HttpsOnly <Boolean?>]`: HttpsOnly: konfigurerar en webbplats så att endast https-begäranden accepteras. Problem med omdirigering för http-begäranden
  - `[HyperV <Boolean?>]`: Hyper-V i begränsat läge.
  - `[IdentityType <ManagedServiceIdentityType?>]`: Typ av identitet för hanterad tjänst.
  - `[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: Listan över användar tilldelade identiteter som är associerade med resursen. Nyckelreferenserna för ordlistan för användaridentitet blir ARM resurs-ID:n i formuläret: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}
    - `[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: Detta anger att alla egenskapen kan läggas till i objektet.
  - `[IsXenon <Boolean?>]`: Föråldrad: Hyper-V (begränsat läge).
  - `[RedundancyMode <RedundancyMode?>]`: Läget Redundans för webbplatsen
  - `[Reserved <Boolean?>]`: <code>true</code> om du har reserverat en plats, <code>false</code> annars.
  - `[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> om du vill stoppa SCM-webbplatsen (KUDU) när appen stoppas, <code>false</code> annars. Standardvärdet är <code>false</code> .
  - `[ServerFarmId <String>]`: Resurs-ID för den associerade apptjänstplanen, formaterad som: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".

## RELATERADE LÄNKAR

