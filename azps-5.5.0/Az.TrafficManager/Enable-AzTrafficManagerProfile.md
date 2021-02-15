---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
ms.openlocfilehash: ba578d800631304405ab1e0a4139a11d9f2a26dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232326"
---
# Enable-AzTrafficManagerProfile

## SYNOPSIS
Aktiverar en traffic manager-profil.

## SYNTAX

### Fält
```
Enable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Objekt
```
Enable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
**Cmdleten Enable-AzTrafficManagerProfile** aktiverar en Azure Traffic Manager-profil.
Du kan ange profilobjektet med hjälp av pipelinen eller som ett parametervärde.
Alternativt kan du ange profilen med hjälp av parametrarna *Namn* och *ResourceGroupName.*

## EXEMPEL

### Exempel 1: Aktivera en profil som anges med namn
```
PS C:\>Enable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

Med det här kommandot aktiveras profilen ContosoProfile i ResourceGroup11.

### Exempel 2: Aktivera en profil med hjälp av pipelinen
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerProfile
```

Med det här kommandot får du profilen ContosoProfile i ResourceGroup11.
Kommandot skickar sedan den profilen till cmdleten **Enable-AzTrafficManagerProfile** med hjälp av rörledningsoperatorn.
Den cmdleten aktiverar den profilen.

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
Anger namnet på profilen i Trafikhanteraren som denna cmdlet aktiverar.

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
Den här cmdleten aktiverar en Traffic Manager-profil i gruppen som den här parametern anger.

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

### -TrafficManagerProfile
Anger ett **TrafficManagerProfile-objekt** som ska aktiveras.
Om du vill **hämta ett TrafficManagerProfile-objekt** använder du Get-AzTrafficManagerProfile cmdleten.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: Object
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

### System.Boolean

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Disable-AzTrafficManagerProfile](./Disable-AzTrafficManagerProfile.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerProfile](./Remove-AzTrafficManagerProfile.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


