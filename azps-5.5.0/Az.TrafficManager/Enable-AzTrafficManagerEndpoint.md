---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 5d7ef8e2fd778b5bcaaea1413bddd85eceb0582c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232334"
---
# Enable-AzTrafficManagerEndpoint

## SYNOPSIS
Aktiverar en slutpunkt i en Trafikhanteraren-profil.

## SYNTAX

### Fält
```
Enable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Objekt
```
Enable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
**Cmdleten Enable-AzTrafficManagerEndpoint** aktiverar en slutpunkt i en Azure Traffic Manager-profil.

Du kan använda en pipelineoperator för att överföra ett **TrafficManagerEndpoint-objekt** till den här cmdleten, eller så kan du ange ett **TrafficManagerEndpoint-objekt** med hjälp av parametern *TrafficManagerEndpoint.*

Du kan också ange slutpunktens namn och  typ  genom att använda parametrarna Namn och Typ tillsammans med *parametrarna ProfileName* och *ResourceGroupName.*

## EXEMPEL

### Exempel 1: Aktivera en slutpunkt från en profil
```
PS C:\>Enable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

Med det här kommandot aktiveras den externa slutpunkten med namnet contoso i profilen ContosoProfile i resursgruppen ResourceGroup11.

### Exempel 2: Aktivera en slutpunkt med hjälp av pipelinen
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerEndpoint
```

Det här kommandot hämtar den externa slutpunkten med namnet Contoso från profilen ContosoProfile i ResourceGroup11.
Kommandot skickar sedan slutpunkten till cmdleten **Enable-AzTrafficManagerEndpoint** med hjälp av rörledningsoperatorn.
Den cmdleten aktiverar den slutpunkten.

## PARAMETERS

### -DefaultProfile
Autentiseringsuppgifterna, kontot, klientorganisationen och prenumerationen som används för kommunikation med Azure.

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

### -Name
Anger namnet på trafikhanterarens slutpunkt som denna cmdlet aktiverar.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProfileName
Anger namnet på en Traffic Manager-profil där den här cmdleten aktiverar en slutpunkt.
Om du vill hämta en profil använder Get-AzTrafficManagerProfile-cmdleten.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på en resursgrupp.
Den här cmdleten aktiverar en slutpunkt för Trafikhanteraren i gruppen som den här parametern anger.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerEndpoint
Anger trafikhanterarens slutpunkt som denna cmdlet aktiverar.
Om du vill **hämta ett TrafficManagerEndpoint-objekt** använder du Get-AzTrafficManagerEndpoint cmdleten.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Type
Anger vilken typ av slutpunkt som denna cmdlet inaktiverar i profilen i Traffic Manager.
Giltiga värden är: 

- AzureEndpoints
- ExternalEndpoints
- NestedEndpoints

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## UTDATA

### System.Boolean

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Disable-AzTrafficManagerEndpoint](./Disable-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[New-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


