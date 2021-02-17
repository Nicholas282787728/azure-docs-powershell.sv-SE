---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: 8f774ab221160a94ee4e8b5f13780b7e3131f252
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216630"
---
# Set-AzTrafficManagerProfile

## SYNOPSIS
Uppdaterar en trafikhanteraren-profil.

## SYNTAX

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
**Cmdleten Set-AzTrafficManagerProfile** uppdaterar en Azure Traffic Manager-profil.
Den här cmdleten uppdaterar inställningarna för profilen från ett lokalt profilobjekt.
Du kan ange profilobjektet antingen med hjälp av *parametern TrafficManagerProfile* eller med hjälp av pipelinen.

Du kan få ett lokalt objekt som representerar en profil med hjälp av Get-AzTrafficManagerProfile cmdleten.
Ändra objektet lokalt och använd sedan **Set-AzTrafficManagerProfile** för att bekräfta ändringarna.

## EXEMPEL

### Exempel 1: Uppdatera en profil
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Det första kommandot får en Azure Traffic Manager-profil med hjälp Get-AzTrafficManagerProfile cmdleten.
Kommandot lagrar profilen lokalt på den $TrafficManagerProfile variabeln.

Det andra kommandot ändrar den profilen lokalt.
Det här kommandot inaktiverar profilen.

Det tredje kommandot uppdaterar trafikhanterarens profil med namnet ContosoProfile så att den matchar det lokala värdet i $TrafficManagerProfile.

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

### -TrafficManagerProfile
Anger ett lokalt **TrafficManagerProfile-objekt.**
Den här cmdleten uppdaterar Trafikhanteraren så att den matchar det här lokala objektet.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
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

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## UTDATA

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Add-AzTrafficManagerEndpointConfig](./Add-AzTrafficManagerEndpointConfig.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpointConfig](./Remove-AzTrafficManagerEndpointConfig.md)

[Remove-AzTrafficManagerProfile](./Remove-AzTrafficManagerProfile.md)


