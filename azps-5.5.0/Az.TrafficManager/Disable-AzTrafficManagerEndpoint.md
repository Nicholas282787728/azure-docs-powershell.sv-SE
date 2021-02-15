---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 037a670c0e96d1a9014cd19b32a7d2ba4da282ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232350"
---
# Disable-AzTrafficManagerEndpoint

## SYNOPSIS
Inaktiverar en slutpunkt i en Traffic Manager-profil.

## SYNTAX

### Fält
```
Disable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Objekt
```
Disable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
**Cmdleten Disable-AzTrafficManagerEndpoint** inaktiverar en slutpunkt i en Azure Traffic Manager-profil.

Du kan använda en pipelineoperator för att överföra ett **TrafficManagerEndpoint-objekt** till den här cmdleten, eller så kan du passera ett **TrafficManagerEndpoint-objekt** med parametern *TrafficManagerEndpoint.*

Du kan också ange slutpunktens namn och  typ  genom att använda parametrarna Namn och Typ tillsammans med *parametrarna ProfileName* och *ResourceGroupName.*

## EXEMPEL

### Exempel 1: Inaktivera en slutpunkt med namn
```
PS C:\> Disable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

Med det här kommandot inaktiveras den externa slutpunkten med namnet contoso i profilen ContosoProfile i resursgruppen ResourceGroup11.
Kommandot uppmanar dig att bekräfta.

### Exempel 2: Inaktivera en slutpunkt med hjälp av pipelinen
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerEndpoint -Force
```

Det här kommandot hämtar den externa slutpunkten med namnet Contoso från profilen ContosoProfile i ResourceGroup11.
Kommandot skickar sedan slutpunkten till cmdleten **Disable-AzTrafficManagerEndpoint** med hjälp av rörledningsoperatorn.
Den cmdleten inaktiverar den slutpunkten.
Kommandot anger *force-parametern.*
Därför uppmanas du inte att bekräfta.

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

### -Force
Tvingar kommandot att köras utan att användaren uppmanas att bekräfta.

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

### -Name
Anger namnet på trafikhanterarens slutpunkt som denna cmdlet inaktiverar.

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
Anger namnet på en Traffic Manager-profil där den här cmdleten inaktiverar en slutpunkt.
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
Den här cmdleten inaktiverar en Trafikhanteraren-slutpunkt i gruppen som den här parametern anger.

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
Anger trafikhanterarens slutpunkt som denna cmdlet inaktiverar.
Om du vill **hämta ett TrafficManagerEndpoint-objekt** använder du Get-AzTrafficManagerEndpoint-cmdleten.

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
Anger vilken typ av slutpunkt som denna cmdlet lägger till i profilen i Trafikhanteraren.
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

### -Bekräfta
Frågar dig om bekräftelse innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
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
Default value: False
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

[Enable-AzTrafficManagerEndpoint](./Enable-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerEndpoint](./Get-AzTrafficManagerEndpoint.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerEndpoint](./New-AzTrafficManagerEndpoint.md)

[New-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


