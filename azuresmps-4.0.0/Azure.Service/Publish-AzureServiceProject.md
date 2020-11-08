---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CF7E7C62-88FC-48CA-940F-9A6C7442BEF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8166cd3faa951171dd3ac865b17b8a03bcefdd45
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099113"
---
# Publish-AzureServiceProject

## Sammanfattning
Publicera den aktuella tjänsten till Windows Azure.

## FRÅGESYNTAXEN

### PublishFromServiceDefinition (standard)
```
Publish-AzureServiceProject [-ServiceName <String>] [-StorageAccountName <String>] [-Location <String>]
 [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>] [-ForceUpgrade]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### PublishFromPackage
```
Publish-AzureServiceProject [-Package <String>] -Configuration <String> [-StorageAccountName <String>]
 [-Location <String>] [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>]
 [-ForceUpgrade] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.
För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .

Cmdleten **Publishing-AzureServiceProject** publicerar den aktuella tjänsten till molnet.
Du kan ange publicerings konfiguration (till exempel **prenumeration** , **StorageAccountName** , **plats** , **fack** ) på kommando raden eller i lokala inställningar via cmdleten **set-AzureServiceProject** .

## BESKRIVS

### Exempel 1: publicera ett service projekt med standardvärden
```
PS C:\> Publish-AzureServiceProject
```

Det här exemplet publicerar den aktuella tjänsten med de aktuella tjänst inställningarna och den aktuella Azure-publicerings profilen.

### Exempel 2: skapa ett distributions paket
```
PS C:\> Publish-AzureServiceProject -PackageOnly
```

I det här exemplet skapas en cspkg-fil (...) i tjänst katalogen och publiceras inte till Windows Azure.

## MALLPARAMETRAR

### -AffinityGroup
Anger den tillhörighets grupp som du vill att tjänsten ska använda.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Konfiguration
Anger tjänstens konfigurations fil.
Om du anger den här parametern anger du *paketet* .

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: cc

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DeploymentName
Anger distributions namnet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: dn

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceUpgrade
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: f

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Lansera
Öppnar ett webbläsarfönster så att du kan se programmet när det har distribuerats.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Plats
Den region där programmet ska hanteras.
Möjliga värden är: 
  
- Världen över
- Överallt i Europa
- Var du än är
- Östasien
- Östra USA
- Norra Central USA
- Nord Europa
- Södra centrala USA
- Sydostasien
- Västeuropa
- Västra USA
 
Om ingen plats anges används platsen i det senaste samtalet till **set-AzureServiceProject** . Om du inte har angett någon plats väljs den slumpmässigt från "norra Central amerikanska" och "Syd Central amerikanska" platser.

```yaml
Type: String
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Paketera
Anger vilken paket fil som ska distribueras.
Ange antingen en lokal fil som har fil namns tillägget. cspkg eller en URI för en blob som innehåller paketet.
Om du anger den här parametern ska du inte ange *ServiceName* -parametern.

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: sp

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser.
Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

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

### -ServiceName
Anger det namn som ska användas för tjänsten när du publicerar till Windows Azure.
Namnet bestämmer en del av etiketten i cloudapp.net-underdomänen som används för att adressera tjänsten när den hanteras i Windows Azure (det vill säga **namn**. cloudapp.net).
Alla namn som anges när tjänsten publiceras åsidosätter namnet som angavs när tjänsten skapades.
(Se cmdleten **New-AzureServiceProject** .

```yaml
Type: String
Parameter Sets: PublishFromServiceDefinition
Aliases: sv

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Plats
Distributions fack för den här tjänsten.
Möjliga värden är ' produktion ' och ' produktion '.
Om du inte anger någon plats används facket i det senaste samtalet till Set-AzureDeploymentSlot.
Om ingen kort plats har angetts används "produktion"-facket.

```yaml
Type: String
Parameter Sets: (All)
Aliases: sl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Anger namnet på Windows Azure Storage-kontot som ska användas när tjänsten publiceras.
Det här värdet används inte förrän tjänsten har publicerats.
När den här parametern inte anges hämtas värdet från det senaste **set-AzureServiceProject-** kommandot.
Om inget lagrings konto har angetts används ett lagrings konto som matchar namnet på tjänsten.
Om det inte finns något sådant lagrings konto försöker cmdleten skapa ett nytt.
Men det går inte att pröva om ett lagrings konto som matchar tjänstens namn finns i en annan prenumeration.

```yaml
Type: String
Parameter Sets: (All)
Aliases: st

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Enable-AzureServiceProjectRemoteDesktop](./Enable-AzureServiceProjectRemoteDesktop.md)

[Set-AzureServiceProject](./Set-AzureServiceProject.md)


