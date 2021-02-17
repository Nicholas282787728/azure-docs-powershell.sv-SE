---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 0000a7a1dba5f175d70fb93631176a49a9da2d13
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216638"
---
# Set-AzTrafficManagerEndpoint

## SYNOPSIS
Uppdaterar en slutpunkt för Trafikhanteraren.

## SYNTAX

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
**Cmdleten Set-AzTrafficManagerEndpoint** uppdaterar en slutpunkt i Azure Traffic Manager.
Den här cmdleten uppdaterar inställningarna från ett lokalt slutpunktsobjekt.
Du kan ange slutpunktsobjektet antingen med hjälp av *parametern TrafficManagerEndpoint* eller med hjälp av pipelinen.

Du kan få ett lokalt objekt som representerar en slutpunkt med hjälp av Get-AzTrafficManagerEndpoint cmdleten.
Ändra objektet lokalt och använd sedan **Set-AzTrafficManagerEndpoint för** att bekräfta ändringarna.

## EXEMPEL

### Exempel 1: Uppdatera en slutpunkt
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Det första kommandot får en Slutpunkt för Azure Traffic Manager med cmdleten **Get-AzTrafficManagerEndpoint.**
Kommandot lagrar slutpunkten lokalt på den $TrafficManagerEndpoint variabeln.

Det andra kommandot ändrar den slutpunkten lokalt.
Det här kommandot ändrar slutpunktens vikt till 20.

Det tredje kommandot uppdaterar slutpunkten i Trafikhanteraren så att den matchar det lokala värdet i $TrafficManagerEndpoint.

## PARAMETERS

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

### -TrafficManagerEndpoint
Anger ett lokalt **TrafficManagerEndpoint-objekt.**
Den här cmdleten uppdaterar Trafikhanteraren så att den matchar det här lokala objektet.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## UTDATA

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## ANTECKNINGAR

## RELATERADE LÄNKAR
