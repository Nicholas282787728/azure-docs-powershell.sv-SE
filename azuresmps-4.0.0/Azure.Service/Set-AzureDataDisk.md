---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 64EF867E-5142-4317-9552-8BC94117208D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 899ecd0256bc3d6f88b8f942fa488db444a9bb41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099296"
---
# Set-AzureDataDisk

## Sammanfattning
Ändrar Host caching för en befintlig data disk på en virtuell Azure-dator.

## FRÅGESYNTAXEN

### NoResize
```
Set-AzureDataDisk [-HostCaching] <String> [-LUN] <Int32> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Ändra storlek på
```
Set-AzureDataDisk [-DiskName] <String> [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzureDataDisk** ändrar cache-attributen för en befintlig datadisk på en virtuell Azure-dator.
Ange vilken datadisk som ska uppdateras med LUN (Logical Unit Number).

## BESKRIVS

### Exempel 1: ändra Host caching för en data disk
```
PS C:\> Get-AzureVM "ContosoService" | Set-AzureDataDisk -VM "VirtualMachine07" -LUN 2 -HostCaching ReadOnly | Update-AzureVM
```

Det här kommandot får de virtuella datorerna som körs på tjänsten som heter ContosoService med hjälp av cmdleten **Get-AzureVM** .
Kommandot skickar dem till den aktuella cmdleten med hjälp av pipeline-operatorn.
Denna cmdlet ställer in data disken på LUN 2 på den virtuella datorn med namnet VirtualMachine07 för att använda ReadOnly-cachelagring för värdar.
Kommandot uppdaterar den virtuella datorn för att återspegla dina ändringar med hjälp av cmdleten **Update-AzureVM** .

### Exempel 2: ändra caching för alla data diskar på en virtuell dator
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk | Set-AzureDataDisk -HostCaching ReadWrite | Update-AzureVM
```

Det här kommandot får ett objekt för den virtuella datorn som heter VirtualMachine07 på ContosoService-moln tjänsten.
Kommandot skickar det till cmdleten **Get-AzureDataDisk** , som hämtar data diskarna för den virtuella datorn.
Den aktuella cmdleten ställer in läget för cachelagring av Host för varje data disk mot ReadWrite.
Kommandot uppdaterar den virtuella datorn för att återspegla dina ändringar.

## MALLPARAMETRAR

### -DiskName
Anger namnet på den data disk konfiguration som denna cmdlet ändrar.

```yaml
Type: String
Parameter Sets: Resize
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching

> [!WARNING]
> Diskcachelagring stöds inte för diskar 4 TiB och senare. Om flera diskar är anslutna till din virtuella dator stöder alla diskar som är mindre än 4 TiB cachelagring.
>
> Ändring av cache-inställningen för en Azure-disk kopplas från och kopplas till mål disketten. Om det är operativ systemets disk startas den virtuella datorn om. Stoppa alla program/tjänster som påverkas av detta avbrott innan du ändrar inställningen för diskcachen. Dessa rekommendationer kan leda till skadade data.

Anger diskens cacheinställningar på nivån.
Giltiga värden är:

- Ingen
- ReadOnly
- Läs

```yaml
Type: String
Parameter Sets: NoResize
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
Anger LUN för data enheten på den virtuella datorn.
Giltiga värden är: 0 till 15.

```yaml
Type: Int32
Parameter Sets: NoResize
Aliases:

Required: True
Position: 1
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

### -ResizedSizeInGB
Anger den nya storleken i GB för data disken.
Den nya storleken måste vara större än den aktuella storleken.

```yaml
Type: Int32
Parameter Sets: Resize
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Anger det virtuella dator objekt som är kopplat till data disken.
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

[Add-AzureDataDisk](./Add-AzureDataDisk.md)

[Get-AzureVM](./Get-AzureVM.md)

[Get-AzureDataDisk](./Get-AzureDataDisk.md)

[Remove-AzureDataDisk](./Remove-AzureDataDisk.md)

[Update-AzureVM](./Update-AzureVM.md)


