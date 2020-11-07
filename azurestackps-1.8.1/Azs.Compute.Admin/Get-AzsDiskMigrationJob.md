---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06f2d231754fc422115cf800ef66189378e0cd4d
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93921744"
---
# Get-AzsDiskMigrationJob

## Sammanfattning
Returnerar listan med hanterade Migreringsverktyg för diskar.

## FRÅGESYNTAXEN

### Lista (standard)
```
Get-AzsDiskMigrationJob [-Status <String>] [-Location <String>] [<CommonParameters>]
```

### ID
```
Get-AzsDiskMigrationJob -ResourceId <String> [<CommonParameters>]
```

### Lära
```
Get-AzsDiskMigrationJob [-Location <String>] -Name <String> [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Returnerar en lista med migreringsjobb.

## BESKRIVS

### --------------------------EXEMPEL 1--------------------------
```
$migration = Get-AzsDiskMigrationJob -location local -Name "mymigrationName"
```

Hämta ett specifikt jobb för hanterad migrering.

### --------------------------EXEMPEL 2--------------------------
```
$migration = Get-AzsDiskMigrationJob -location local
```

Returnerar en lista med hanterade diskallokering på platsen lokal.

## MALLPARAMETRAR

### -Plats
Plats för resursen.

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
GUID-namnet för migreringen.

```yaml
Type: String
Parameter Sets: Get
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Resurs-ID.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Status
Parametrarna för jobb status för diskallokering.

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

### Microsoft. AzureStack. Management. Compute. admin. Models. DiskMigrationJob

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

