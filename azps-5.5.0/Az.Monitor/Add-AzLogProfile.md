---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: bc0f1a6aacc6188a982fe75fa021bdafdc4e02de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219054"
---
# Add-AzLogProfile

## SYNOPSIS
Skapar en ny aktivitetsloggprofil. Den här profilen används för att antingen arkivera aktivitetsloggen till ett Azure-lagringskonto eller strömma den till ett Azure-händelsenav i samma prenumeration. 

## SYNTAX

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Add-AzLogProfile** skapar en loggprofil.
- **Lagringskonto** – Endast standardlagringskonto (premiumlagringskonto stöds inte) stöds. Det kan vara av typen ARM eller klassisk. Om den loggas på ett lagringskonto debiteras kostnaden för aktivitetsloggen enligt normala lagringskostnader. Det kan bara finnas en loggprofil per följd av prenumerationen, men bara ett lagringskonto per prenumeration kan användas för att exportera aktivitetsloggen. 
- **Händelsehubben** – Det kan bara finnas en loggprofil per följd av prenumerationen, men bara ett händelsenav per prenumeration kan användas för att exportera aktivitetsloggen. Om aktivitetsloggen strömmas till ett händelsenav gäller standardpris för händelsenav. I aktivitetsloggen kan händelser gälla en region eller vara "globala". Globala innebär i princip att dessa händelser är region-agnostics och är oberoende av region, och att majoriteten av händelserna faller inom den här kategorin. Om aktivitetsloggprofilen anges från portalen läggs "Global" automatiskt till tillsammans med ett annat område som väljs i användargränssnittet. När du använder cmdleten måste platsen som "Global" uttryckligen omnämnas förutom andra regioner. 
**Obs!** Om du inte anger "Global" på platserna leder det till att majoriteten av **aktivitetsloggen inte exporteras.** Den här cmdleten implementerar mönstret ShouldProcess, dvs. den kan begära bekräftelse från användaren innan den faktiskt skapar, ändrar eller tar bort resursen.

## EXEMPEL

### Exempel 1: Lägga till en ny loggprofil för att exportera aktivitetsloggen som matchar platsvillkoret till ett lagringskonto
```powershell
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

### Exempel 2

Skapar en ny aktivitetsloggprofil. (autogenererat)

```powershell <!-- Aladdin Generated Example --> 
Add-AzLogProfile -Location 'Global' -Name ExportLogProfile -RetentionInDays <Int32> -ServiceBusRuleId <String> -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## PARAMETERS

### -Kategori
Anger listan med kategorier.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plats
Anger loggprofilens plats.
Giltiga värden: Kör under cmdleten för att få den senaste listan över platser. Get-AzLocation | Välj Visningsnamn

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Anger namnet på profilen.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionInDays
Anger bevarandeprincipen i dagar. Det här är det antal dagar som loggarna behålls i det angivna lagringskontot. Om du vill behålla data ska du alltid ange **detta till 0.** Om den inte anges blir 0 som **standard.** Normala faktureringssatser för lagring av data eller händelsenav gäller för datalagring.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceBusRuleId
Anger ID för Service Bus-regeln.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountId
Anger ID för lagringskontot. ID är det fullständigt kvalificerade resurs-ID:t för lagringskontot, till exempel  
/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Frågar dig om bekräftelse innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som skulle hända om cmdleten körs. Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## UTDATA

### Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzLogProfile](./Get-AzLogProfile.md)

[Remove-AzLogProfile](./Remove-AzLogProfile.md)


