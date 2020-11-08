---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 50B83AEC-1B32-4089-9804-D388677C3F7E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7388841c48f2f7c6ba0752748b245cce1f8b5c4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099322"
---
# Remove-AzureTrafficManagerEndpoint

## Sammanfattning
Tar bort en slut punkt från en Traffic Manager-profil.

## FRÅGESYNTAXEN

```
Remove-AzureTrafficManagerEndpoint -DomainName <String> [-Force]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzureTrafficManagerEndpoint** tar bort en slut punkt från en Microsoft Azure Traffic Manager-profil.
När du har tagit bort en slut punkt skickar du resultatet till cmdleten **set-AzureTrafficManagerProfile** med hjälp av pipeline-operatorn.
Denna cmdlet ansluter till Azure för att spara dina ändringar.

## BESKRIVS

### Exempel 1: ta bort en slut punkt från en profil
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Remove-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" | Set-AzureTrafficManagerProfile
```

Det första kommandot använder cmdleten **Get-AzureTrafficManagerProfile** för att hämta profilen med namnet ContosoProfile och lagrar den sedan i $TrafficManagerProfile variabel.

Det andra kommandot tar bort en slut punkt som innehåller domän namnet Contoso02App.cloudapp.net från Traffic Manager-profilen som lagras i $TrafficManagerProfile.
Kommandot skickar Profile-objektet till cmdleten **set-AzureTrafficManagerProfile** för att ansluta till Azure för att spara ändringarna.

## MALLPARAMETRAR

### -Domän namn
Anger domän namnet för slut punkten som ska tas bort.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
```yaml
Type: SwitchParameter
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

### -TrafficManagerProfile
Anger den Traffic Manager-profil som du vill ta bort slut punkten från.

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. WindowsAzure. commands. Utilities. TrafficManager. Models. IProfileWithDefinition
Denna cmdlet skapar ett profil objekt för Traffic Manager, som innehåller information om den uppdaterade profilen.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureTrafficManagerEndpoint](./Add-AzureTrafficManagerEndpoint.md)

[Set-AzureTrafficManagerEndpoint](./Set-AzureTrafficManagerEndpoint.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


