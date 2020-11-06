---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: 7944328c7cac37d88cf18d715cbb7a893eacc683
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576377"
---
# Remove-AzureRmTrafficManagerEndpointConfig

## Sammanfattning
Tar bort en slut punkt från ett lokalt Traffic Manager-Profile-objekt.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Remove-AzureRmTrafficManagerEndpointConfig -EndpointName <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Remove-AzureRmTrafficManagerEndpointConfig** tar bort en slut punkt från ett lokalt Azure Traffic Manager-Profile-objekt.
Du kan hämta en profil med hjälp av Get-AzureRmTrafficManagerProfile cmdlet.

Denna cmdlet fungerar på det lokala profilens objekt.
Bekräfta dina ändringar av profilen för Traffic Manager genom att använda Set-AzureRmTrafficManagerProfile cmdlet.
Om du vill ta bort en slut punkt och verkställa ändringar i en enskild åtgärd kan du använda Remove-AzureRmTrafficManagerEndpoint cmdlet.

## BESKRIVS

### Exempel 1: ta bort en slut punkt
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -Type AzureEndpoints -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Det första kommandot får en Azure Traffic Manager-profil genom att använda cmdleten **Get-AzureRmTrafficManagerProfile** .
Kommandot lagrar den lokala profilen i $TrafficManagerProfile variabel.

Det andra kommandot tar bort en Azure-slutpunkt med namnet contoso från profilen som lagras i $TrafficManagerProfile.
Det här kommandot ändrar bara det lokala objektet.

Det sista kommandot uppdaterar Traffic Manager-profilen med namnet ContosoProfile för att matcha det lokala värdet i $TrafficManagerProfile.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndpointName
Anger namnet på den trafik hanterarens slut punkt som denna cmdlet tar bort.

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

### -TrafficManagerProfile
Anger ett lokalt **TrafficManagerProfile** -objekt.
Denna cmdlet ändrar detta lokala objekt.
För att hämta ett **TrafficManagerProfile** -objekt, Använd cmdleten Get-AzureRmTrafficManagerProfile.

```yaml
Type: TrafficManagerProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft. Azure. commands. Network. TrafficManagerProfile
Denna cmdlet accepterar ett **TrafficManagerProfile** -objekt till denna cmdlet.

## VÄRDEN

### Microsoft. Azure. commands. Network. TrafficManagerProfile
Denna cmdlet returnerar ett ändrat TrafficManagerProfile-objekt.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureRmTrafficManagerEndpointConfig](./Add-AzureRmTrafficManagerEndpointConfig.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[Remove-AzureRmTrafficManagerEndpoint](./Remove-AzureRmTrafficManagerEndpoint.md)

[Set-AzureRmTrafficManagerProfile](./Set-AzureRmTrafficManagerProfile.md)


