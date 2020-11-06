---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 896324e8d08cae69f24c195de9b44b325985c2c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576380"
---
# New-AzureRmTrafficManagerProfile

## Sammanfattning
Skapar en Traffic Manager-profil.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
New-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureRmTrafficManagerProfile** skapar en Azure Traffic Manager-profil.
Ange parametern *Name* och nödvändiga inställningar.
Denna cmdlet returnerar ett lokalt objekt som representerar den nya profilen.

Denna cmdlet konfigurerar inte slut punkter för Traffic Manager.
Du kan uppdatera det lokala profil objektet med hjälp av Add-AzureRmTrafficManagerEndpointConfig cmdlet.
Överför sedan ändringar till Traffic Manager med hjälp av Set-AzureRmTrafficManagerProfile cmdlet.
Du kan också lägga till slut punkter med New-AzureRmTrafficManagerEndpoint cmdlet.

## BESKRIVS

### Exempel 1: skapa en profil
```
PS C:\>New-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

Det här kommandot skapar en Azure Traffic Manager-profil med namnet ContosoProfile i resurs grupp ResourceGroup11.
DNS FQDN är contosoapp.trafficmanager.net.

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

### -MonitorIntervalInSeconds
Intervallet (i sekunder) som trafik hanteraren kontrollerar tillståndet för varje slut punkt i den här profilen. Standardvärdet är 30.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: IntervalInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorPath
Anger sökvägen som används för att övervaka slut punktens status.
Ange ett värde relativt till slut punkts domän namnet.
Värdet måste börja med ett snedstreck (/).

```yaml
Type: String
Parameter Sets: (All)
Aliases: PathForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorPort
Anger den TCP-port som används för att övervaka slut punktens status.
Giltiga värden är heltal från 1 till 65535.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: PortForMonitor

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorProtocol
Anger vilket protokoll som ska användas för att övervaka slut punktens status.
Giltiga värden är:

- INKOMMANDE
- HTTPS

```yaml
Type: String
Parameter Sets: (All)
Aliases: ProtocolForMonitor
Accepted values: HTTP, HTTPS, TCP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorTimeoutInSeconds
Den tid (i sekunder) som trafik hanteraren tillåter slut punkter i den här profilen för att svara på hälso kontrollen. Standardvärdet är 10.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: TimeoutInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorToleratedNumberOfFailures
Antalet misslyckade hälso kontroller på flera nivåer i trafik hanteraren innan en slut punkt i den här profilen deklareras efter nästa misslyckade hälso kontroll. Standardvärdet är 3.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ToleratedNumberOfFailuresForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger ett namn för Traffic Manager-profilen som denna cmdlet skapar.

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

### -ProfileStatus
Anger statusen för profilen.
Giltiga värden är: Enabled och disabled.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RelativeDnsName
Anger det relativa DNS-namnet som den här Traffic Manager-profilen ger.
Traffic Manager kombinerar det här värdet och det DNS-domännamn som Azure Traffic Manager använder för att skapa det fullständigt kvalificerade domän namnet (FQDN) för profilen.

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

### -ResourceGroupName
Anger namnet på en resurs grupp.
Den här cmdleten skapar en Traffic Manager-profil i gruppen som den här parametern anger.

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

### -Tagg
Par med nyckelord i en hash-tabell som taggar på servern. Till exempel:

@ {key0 = "value0"; KEY1 = $null; key2 = "värde2"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficRoutingMethod
Anger metoden för trafik cirkulation.
Den här metoden avgör vilken slut punkts Traffic Manager returnerar som svar på inkommande DNS-frågor.
Giltiga värden är:

- Prestandaräknare
- Viktat
- Ordningen
- Visio

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Performance, Weighted, Priority, Geographic

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TTL
Anger TTL-värdet (Time to Live) för DNS.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### Microsoft. Azure. commands. Network. TrafficManagerProfile
Denna cmdlet returnerar ett nytt TrafficManagerProfile-objekt.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureRmTrafficManagerEndpointConfig](./Add-AzureRmTrafficManagerEndpointConfig.md)

[Disable-AzureRmTrafficManagerProfile](./Disable-AzureRmTrafficManagerProfile.md)

[Enable-AzureRmTrafficManagerProfile](./Enable-AzureRmTrafficManagerProfile.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[Remove-AzureRmTrafficManagerProfile](./Remove-AzureRmTrafficManagerProfile.md)

[Set-AzureRmTrafficManagerProfile](./Set-AzureRmTrafficManagerProfile.md)


