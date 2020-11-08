---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 48211644-1B92-443D-A992-BDF517D89341
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49b4039e07cf9f393a85c9592598ad870586fd06
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94100660"
---
# Get-WAPackVMSizeProfile

## Sammanfattning
Ändrar profilernas storlek.

## FRÅGESYNTAXEN

### Tom (standard)
```
Get-WAPackVMSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromId
```
Get-WAPackVMSizeProfile [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromName
```
Get-WAPackVMSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
De här ämnena är föråldrade och kommer att tas bort i framtiden.
I det här avsnittet beskrivs cmdleten i 0.8.1-versionen av Microsoft Azure PowerShell-modulen.
För att ta reda på vilken version av modulen du använder, går du till Azure PowerShell-konsolen och skriver `(Get-Module -Name Azure).Version` .

Cmdleten **Get-WAPackVMSizeProfile** ändrar storlek på profil objekt för virtuella datorer.

## BESKRIVS

### Exempel 1: få en storleks profil genom att använda ett namn
```
PS C:\> Get-WAPackVMSizeProfile -Name "ContosoSizeProfile07"
```

Det här kommandot får storleks profilen ContosoSizeProfile07.

### Exempel 2: skapa en storleks profil med hjälp av ett ID
```
PS C:\> Get-WAPackVMSizeProfile -ID 66242D17-189F-480D-87CF-8E1D749998C8
```

Det här kommandot får storleks profilen med angivet ID.

### Exempel 3: Hämta alla storleks profiler
```
PS C:\> Get-WAPackVMSizeProfile
```

Det här kommandot får alla storleks profiler.

## MALLPARAMETRAR

### -ID
Anger ett unikt ID för en storleks profil.

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger namnet på en storleks profil.

```yaml
Type: String
Parameter Sets: FromName
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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

## VÄRDEN

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-WAPackVM](./Get-WAPackVM.md)


