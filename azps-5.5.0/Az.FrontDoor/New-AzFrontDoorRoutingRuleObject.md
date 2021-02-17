---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorroutingruleobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorRoutingRuleObject.md
ms.openlocfilehash: f50aa9099a3bcc5e6137f9f705a05e4d26e693d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234367"
---
# New-AzFrontDoorRoutingRuleObject

## SYNOPSIS
Skapa en PSRoutingRuleObject för att skapa en framsida

## SYNTAX

### ByFieldsWithForwardingParameterSet (Standard)
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> -BackendPoolName <String> [-AcceptedProtocol <PSProtocol[]>]
 [-PatternToMatch <String[]>] [-CustomForwardingPath <String>] [-ForwardingProtocol <String>]
 [-EnableCaching <Boolean>] [-QueryParameterStripDirective <String>] [-DynamicCompression <PSEnabledState>]
 [-EnabledState <PSEnabledState>] [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByFieldsWithRedirectParameterSet
```
New-AzFrontDoorRoutingRuleObject -ResourceGroupName <String> -FrontDoorName <String> -Name <String>
 -FrontendEndpointName <String[]> [-AcceptedProtocol <PSProtocol[]>] [-PatternToMatch <String[]>]
 [-RedirectType <String>] [-RedirectProtocol <String>] [-CustomHost <String>] [-CustomPath <String>]
 [-CustomFragment <String>] [-CustomQueryString <String>] [-EnabledState <PSEnabledState>]
 [-RulesEngineName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Skapa en PSRoutingRuleObject för att skapa en framsida

## EXEMPEL

### Exempel 1: Skapa en PSRoutingRuleObject för att skapa en front door med en vidarebefordraingsregel
```powershell
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName $rgname -FrontendEndpointName "frontendEndpoint1" -BackendPoolName "backendPool1" 

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
HealthProbeSettings          :
RouteConfiguration           : Microsoft.Azure.Commands.FrontDoor.Models.PSForwardingConfiguration
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : {routingRuleName}
Type                         :
```

### Exempel 2: Skapa en PSRoutingRuleObject för att skapa en front door med en omdirigeringsregel
```powershell
PS C:\> $customHost = "www.contoso.com"
PS C:\> $customPath = "/images/contoso.png"
PS C:\> $queryString = "field1=value1&field2=value2"
PS C:\> $destinationFragment = "section-header-2"
PS C:\> New-AzFrontDoorRoutingRuleObject -Name $routingRuleName -FrontDoorName $frontDoorName -ResourceGroupName $rgname -FrontendEndpointName "frontendEndpoint1" -CustomHost $customHost -CustomPath $customPath -CustomQueryString $queryString -CustomFragment $destinationFragment

FrontendEndpointIds          : {/subscriptions/{subid}/resourceGroups/{rgname}/pro
                               viders/Microsoft.Network/frontDoors/{frontdoorname}/FrontendEndpoints/frontendEndpoint1}
AcceptedProtocols            : {Http, Https}
PatternsToMatch              : {/*}
HealthProbeSettings          :
RouteConfiguration           : Microsoft.Azure.Commands.FrontDoor.Models.PSRedirectConfiguration
EnabledState                 : Enabled
ResourceState                :
Id                           :
Name                         : {routingRuleName}
Type                         :
```

Skapa en PSRoutingRuleObject för att skapa en framsida

## PARAMETERS

### -AcceptedProtocol
Protokollscheman som ska matcha för den här regeln.
Standardvärdet är {https, http}

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendPoolName
Resurs-ID för BackendPool som den här regeln dirigerar till

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomForwardingPath
Den anpassade sökväg som används för att skriva om resurssökvägar matchade med den här regeln.
Lämna tomt för att använda inkommande sökväg.

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomFragment
Fragment som ska läggas till i omdirigerings-URL:en. Fragment är den del av URL-adressen som kommer efter #. Ta inte med felvärdet #.

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomHost
Värd som ska omdirigeras. Lämna tomt om du vill använda den inkommande värden som målvärd.

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomPath
Den fullständiga sökvägen till omdirigering. Sökvägen kan inte vara tom och måste börja med /. Lämna den tomma om du vill använda den inkommande sökvägen som målsökväg.

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomQueryString
Den uppsättning frågesträngar som ska placeras i omdirigerings-URL:en. Om du anger det här värdet ersätts alla befintliga frågesträngar. lämna tomt för att bevara den inkommande frågesträngen. Frågesträngen måste vara i <key>=<value> format. Den första ? och & automatiskt så inkludera dem inte längst fram, men avgränsa flera frågesträngar med &.

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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

### -DynamicCompression
Om dynamisk komprimering ska aktiveras för cachelagrat innehåll när cachelagring är aktiverat.
Standardvärdet är aktiverat

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableCaching
Om du vill aktivera cachelagring för den här vägen. Standardvärdet är falskt

```yaml
Type: System.Boolean
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnabledState
Om regeln ska användas.
Standardvärdet är aktiverat

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForwardingProtocol
Det protokoll som används av den här regeln när trafik vidarebefordras till backends Standardvärde är MatchRequest.

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FrontDoorName
Namnet på den front door som den här routningsregeln tillhör.

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

### -FrontendEndpointName
Namnen på klientslutpunkterna som är kopplade till den här regeln

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

### -Name
RoutingRule name.

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

### -PatternToMatch
Regelns routemönster får inte ha någon * förutom eventuellt efter den sista /i slutet av sökvägen. Standardvärdet är /*

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

### -QueryParameterStripDirective
Hur URL-frågetermer används när cachenyckeln skapas.
Standardvärdet är StripAll

```yaml
Type: System.String
Parameter Sets: ByFieldsWithForwardingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectProtocol
Protokollet för målet dit trafiken omdirigeras. Standardvärdet är MatchRequest

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectType
Den omdirigeringstyp som regeln kommer att använda när du omdirigerar trafik. Standardvärdet flyttas

```yaml
Type: System.String
Parameter Sets: ByFieldsWithRedirectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Resursgruppnamnet som RoutingRule ska skapas i.

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

### -RulesEngineName
En referens till en specifik regelmotorkonfiguration som ska gälla för den här vägen.

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

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Ingen

## UTDATA

### Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule

## ANTECKNINGAR

## RELATERADE LÄNKAR

[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)
