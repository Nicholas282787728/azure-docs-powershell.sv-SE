---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3B3F1870-348D-4303-9520-FD81D4650F5F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2103a155b12fdf1e481173d529ff3308a3b2200b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099742"
---
# Get-AzureWebHostingPlan

## Sammanfattning
Hämtar Azure Web Hosting-abonnemang i det aktuella abonnemanget.

## FRÅGESYNTAXEN

```
Get-AzureWebHostingPlan [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.
För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .

Cmdleten **Get-AzureWebHostingPlan** får Azure Web Hosting-abonnemangen i det aktuella abonnemanget.

Som standard får **Get-AzureWebHostingPlan** alla Azure hosting-abonnemang i det aktuella abonnemanget och returnerar ett objekt med grundläggande information om abonnemangen.
När du använder parametrarna *webspace* och *Name* returnerar **-AzureWebHostingPlan** ett specifikt värd Plans objekt.

Använd den *aktuella* parametern för cmdleten **Get-AzureSubscription** för att hitta den aktuella prenumerationen.
Använd cmdleten **Select-AzureSubscription** för att ändra aktuell prenumeration.

## BESKRIVS

### Exempel 1: skaffa alla webbhotell i ett abonnemang
```
PS C:\> Get-AzureWebHostingPlan 

Name : Default1 
SKU : Basic 
WorkerSize : Small 
NumberOfWorkers : 1 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 1 
Status : Ready 
WebSpace : eastuswebspace 
Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready
```

Det här kommandot får alla Azure Web Hosting-abonnemang i det aktuella abonnemanget.

### Exempel 2: skaffa ett visst webb värd abonnemang i ett abonnemang
```
PS C:\> Get-AzureWebHostingPlan -WebSpaceName "westeuropewebspace" -Name "Default0" 

Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready 
WebSpace : westeuropewebspace
```

Det här kommandot hämtar webb värd planen med namnet Default0 i det webspace som heter westeuropewebspace i det aktuella abonnemanget.

## MALLPARAMETRAR

### -Namn
Anger namnet på en plan i prenumerationen.
Som standard får denna cmdlet alla planer i den aktuella prenumerationen.
Den här parametern stöder inte jokertecken.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

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

### -WebSpaceName
Anger namnet på ett webbområde i prenumerationen.
Som standard hämtar denna cmdlet alla webbplatser i angivet Webspace.
Den här parametern stöder inte jokertecken.

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

###  
Du kan skicka data till denna cmdlet efter egenskaps namn, men inte efter värde.

## VÄRDEN

### Microsoft. WindowsAzure. commands. Utilities. webentities. WebHostingPlan
Som standard returnerar **Get-AzureWebHostingPlan** en matris med **WebHostingPlan** -objekt.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

