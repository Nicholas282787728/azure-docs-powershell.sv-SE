---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 58811a34a2f3d2b4684813c42723a5cab354a13f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581887"
---
# Set-AzureRmTrafficManagerProfile

## Sammanfattning
Uppdaterar en Traffic Manager-profil.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Set-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureRmTrafficManagerProfile** uppdaterar en Azure Traffic Manager-profil.
Denna cmdlet uppdaterar inställningarna för profilen från ett lokalt profil objekt.
Du kan ange ett profil objekt antingen med hjälp av parametern *TrafficManagerProfile* eller genom att använda pipeline.

Du kan få ett lokalt objekt som representerar en profil med hjälp av Get-AzureRmTrafficManagerProfile cmdlet.
Ändra objektet lokalt och Använd sedan **set-AzureRmTrafficManagerProfile** för att bekräfta dina ändringar.

## BESKRIVS

### Exempel 1: uppdatera en profil
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Det första kommandot får en Azure Traffic Manager-profil med hjälp av Get-AzureRmTrafficManagerProfile cmdlet.
Kommandot lagrar profilen lokalt i $TrafficManagerProfile variabel.

Det andra kommandot ändrar profilen lokalt.
Det här kommandot inaktiverar profilen.

Det tredje kommandot uppdaterar Traffic Manager-profilen med namnet ContosoProfile för att matcha det lokala värdet i $TrafficManagerProfile.

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

### -TrafficManagerProfile
Anger ett lokalt **TrafficManagerProfile** -objekt.
Denna cmdlet uppdaterar trafik hanteraren så att den matchar detta lokala objekt.

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
Denna cmdlet accepterar ett **TrafficManagerProfile** -objekt.

## VÄRDEN

### Microsoft. Azure. commands. Network. TrafficManagerProfile
Denna cmdlet returnerar ett **TrafficManagerProfile** -objekt.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureRmTrafficManagerEndpointConfig](./Add-AzureRmTrafficManagerEndpointConfig.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[New-AzureRmTrafficManagerProfile](./New-AzureRmTrafficManagerProfile.md)

[Remove-AzureRmTrafficManagerEndpointConfig](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[Remove-AzureRmTrafficManagerProfile](./Remove-AzureRmTrafficManagerProfile.md)


