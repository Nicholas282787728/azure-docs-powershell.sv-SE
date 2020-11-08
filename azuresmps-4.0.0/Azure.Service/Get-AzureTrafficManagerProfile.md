---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 28136DC3-520B-4134-8736-93D86EEABAE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf9fd7b67b63ce2bddb762c7006722b6035ffe87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093262"
---
# Get-AzureTrafficManagerProfile

## Sammanfattning
Hämtar information om en Traffic Manager-profil.

## FRÅGESYNTAXEN

```
Get-AzureTrafficManagerProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureTrafficManagerProfile** får information om en profil i Microsoft Azure Traffic Manager.
Om du inte anger parametern *Name* visar cmdleten Traffic Manager-profilerna i den aktuella prenumerationen.

## BESKRIVS

### Exempel 1: hämta listan med profiler för Traffic Manager i ett abonnemang
```
PS C:\>Get-AzureTrafficManagerProfile
```

Det här kommandot får listan över Traffic Manager-profiler i ditt abonnemang.

### Exempel 2: skaffa en Traffic Manager-profil
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile"
```

Det här kommandot får Traffic Manager-profilen som heter min-profil.

### Exempel 3: lägga till en slut punkt till en Traffic Manager-profil
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Add-AzureTrafficManagerEndpoint -DomainName "Myapp2.cloudapp.net" -TrafficManagerProfile $MyTrafficManagerProfile -Type "CloudService" -Status "Enabled" | Set-AzureTrafficManagerProfile
```

Det här kommandot lägger till en slut punkt till en Traffic Manager-profil och sparar sedan profilen.

## MALLPARAMETRAR

### -Namn
Anger namnet på den Traffic Manager-profil som ska visas.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser. Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. WindowsAzure. commands. Utilities. TrafficManager. Models. IProfileWithDefinition
Denna cmdlet skapar ett profil objekt eller objekt för Traffic Manager.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureTrafficManagerEndpoint](./Add-AzureTrafficManagerEndpoint.md)

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[New-AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


