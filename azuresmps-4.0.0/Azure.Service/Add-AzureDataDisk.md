---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FDEDBF4F-7507-43FF-A983-7E431C0C1950
online version: ''
schema: 2.0.0
ms.openlocfilehash: 967fbaf83efa12bd305fc9fe075a9abffdd62dc3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093461"
---
# Add-AzureDataDisk

## Sammanfattning
Lägger till en datadisk till en virtuell dator.

## FRÅGESYNTAXEN

### CreateNew (standard)
```
Add-AzureDataDisk [-CreateNew] [-DiskSizeInGB] <Int32> [-DiskLabel] <String> [-LUN] <Int32>
 [-MediaLocation <String>] [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Importeras
```
Add-AzureDataDisk [-Import] [-DiskName] <String> [-LUN] <Int32> [-HostCaching <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### ImportFrom
```
Add-AzureDataDisk [-ImportFrom] [-DiskLabel] <String> [-LUN] <Int32> -MediaLocation <String>
 [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Add-AzureDataDisk** lägger till en ny eller befintlig datadisk till ett objekt i Azure Virtual Machine.
Använd parametern *createnew* för att skapa en ny data skiva med angiven storlek och etikett.
Använd *import* parametern för att bifoga en befintlig disk från bild lagrings platsen.
Använd parametern *ImportFrom* för att bifoga en befintlig disk från en BLOB i ett lagrings konto.
Du kan ange värd-cache-läget för den anslutna data disken.

## BESKRIVS

### Exempel 1: importera en data disk från databasen
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Add-AzureDataDisk -Import -DiskName "Disk68" -LUN 0 | Update-AzureVM
```

Det här kommandot får ett virtuellt dator objekt för den virtuella datorn med namnet VirtualMachine07 i ContosoService-moln tjänsten genom att använda cmdleten **Get-AzureVM** .
Kommandot skickar det till den aktuella cmdleten med hjälp av pipeline-operatorn.
Det kommandot kopplar en befintlig datadisk från databasen till den virtuella datorn.
Data disken har en LUN på 0.
Kommandot uppdaterar den virtuella datorn för att återspegla dina ändringar med hjälp av cmdleten **Update-AzureVM** .

### Exempel 2: lägga till en ny data skiva
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine08" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 128 -DiskLabel "main" -LUN 0 | Update-AzureVM
```

Det här kommandot får ett virtuellt dator objekt för den virtuella datorn med namnet VirtualMachine08.
Kommandot skickar det till den aktuella cmdleten.
Kommandot bifogar en ny data skiva med namnet MyNewDisk. VHD.
Cmdleten skapar disken i behållaren VHD: er i det vanliga lagrings kontot för den aktuella prenumerationen.
Kommandot uppdaterar den virtuella datorn för att återspegla dina ändringar.

### Exempel 3: lägga till en datadisk från en angiven plats
```
PS C:\> Get-AzureVM "ContosoService" -Name "Database" | Add-AzureDataDisk -ImportFrom -MediaLocation "https://contosostorage.blob.core.windows.net/container07/Disk14.vhd" -DiskLabel "main" -LUN 0 | Update-AzureVM
```

Det här kommandot får ett virtuellt dator objekt för den virtuella datorn med namnet Database.
Kommandot skickar det till den aktuella cmdleten.
Kommandot kopplar en befintlig datadisk med namnet Disk14. VHD från den angivna platsen.
Kommandot uppdaterar den virtuella datorn för att återspegla dina ändringar.

## MALLPARAMETRAR

### -CreateNew
Anger att denna cmdlet skapar en data disk.

```yaml
Type: SwitchParameter
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskLabel
Anger disk etiketten för en ny data disk.

```yaml
Type: String
Parameter Sets: CreateNew, ImportFrom
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskName
Anger namnet på en data disk i disk lagringen.

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskSizeInGB
Anger storleken på logiska diskar för en ny data disk i GB.

```yaml
Type: Int32
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching
Anger diskens cacheinställningar på nivån.
Giltiga värden är: 

- Ingen 
- ReadOnly 
- Läs

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

### -Importera
Anger att denna cmdlet importerar en befintlig data disk från bild lagrings platsen.

```yaml
Type: SwitchParameter
Parameter Sets: Import
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImportFrom
Anger att denna cmdlet importerar en befintlig data disk från en blob till ett lagrings konto.

```yaml
Type: SwitchParameter
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
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

### -LUN
Anger LUN (Logical Unit Number) för data enheten på den virtuella datorn.
Giltiga värden är: 0 till 15.
Varje data disk måste ha ett unikt LUN.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaLocation
Anger platsen för blobben i ett Azure Storage-konto där denna cmdlet lagrar data disken.
Om du inte anger en plats lagras data disken i behållaren VHD: er i standard lagrings kontot för den aktuella prenumerationen.
Om det inte finns en behållare för virtuella hård diskar skapas en behållare för virtuella hård diskar.

```yaml
Type: String
Parameter Sets: CreateNew
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportFrom
Aliases: 

Required: True
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

### -VM
Anger det virtuella dator objekt som denna cmdlet ansluter en data disk till.
Använd cmdleten **Get-AzureVM** för att hämta ett virtuellt dator objekt.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

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

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureDataDisk](./Get-AzureDataDisk.md)

[Get-AzureVM](./Get-AzureVM.md)

[Remove-AzureDataDisk](./Remove-AzureDataDisk.md)

[Set-AzureDataDisk](./Set-AzureDataDisk.md)

[Update-AzureVM](./Update-AzureVM.md)


