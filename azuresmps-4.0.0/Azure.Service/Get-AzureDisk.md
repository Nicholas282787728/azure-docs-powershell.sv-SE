---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95DCD2EC-8327-4A46-B624-289D0A28F7EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4614910b8c0ccd36bb8ef75ee98f662cf69a276a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099584"
---
# Get-AzureDisk

## Sammanfattning
Hämtar information om diskar i Azure-lagringsplatsen.

## FRÅGESYNTAXEN

```
Get-AzureDisk [[-DiskName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureDisk** hämtar information om de diskar som lagras i Azure-lagringsplatsen för det aktuella abonnemanget.
Denna cmdlet returnerar en lista med information för alla diskar i databasen.
Om du vill visa information om en viss disk anger du namnet på disken.

## BESKRIVS

### Exempel 1: Hämta information om en disk
```
PS C:\> Get-AzureDisk -DiskName "ContosoDataDisk"
```

Det här kommandot hämtar information om den disk som heter ContosoDataDisk från diskens lagrings plats.

### Exempel 2: få information om alla diskar
```
PS C:\> Get-AzureDisk
```

Med det här kommandot får du information om alla diskar i disk lagringen.

### Exempel 3: Hämta information om en disk
```
PS C:\> Get-AzureDisk | Where-Object {$_.AttachedTo -eq $Null } | Format-Table -AutoSize -Property "DiskName","DiskSizeInGB","MediaLink"
```

Det här kommandot hämtar data för alla diskar i disk lagrings platsen som för närvarande inte är anslutna till en virtuell dator.
Med kommandot får du information om alla diskar och skickar objekten till cmdleten **WHERE-objekt** .
Denna cmdlet tar alla diskar som inte har värdet $Null för egenskapen **AttachedTo** .
Kommandot formaterar listan som en tabell med hjälp av cmdleten **Format-Table** .

## MALLPARAMETRAR

### -DiskName
Anger namnet på den disk i disk lagringen där denna cmdlet hämtar information.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InformationAction
Anger hur den här cmdleten svarar på en informations händelse.

De acceptabla värdena för den här parametern är:

- Vidare
- Över
- Inquire
- SilentlyContinue
- Stanna
- Avbryt

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Anger en informations variabel.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Add-AzureDisk](./Add-AzureDisk.md)

[Remove-AzureDisk](./Remove-AzureDisk.md)

[Update-AzureDisk](./Update-AzureDisk.md)


