---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLog.md
ms.openlocfilehash: 90f65c7e3db862ca4d24b67187f587511593be4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576986"
---
# Get-AzureRmLog

## Sammanfattning
Hämtar en logg över händelser.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### GetByCorrelationId
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceId
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceGroup
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceProvider
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetBySubscription
```
Get-AzureRmLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmLog** hämtar en logg över händelser.
Händelserna kan associeras med aktuellt prenumerations-ID, korrelations-ID, resurs grupp, resurs-ID eller resurs leverantör.

## BESKRIVS

### Exempel 1: Hämta en händelse logg efter abonnemangs-ID
```
PS C:\>Get-AzureRmLog
```

Det här kommandot listar de flesta 1000-händelser som är kopplade till användarens prenumerations-ID som tog sju dagar från dagens datum/tid.

### Exempel 2: Hämta en händelse logg per prenumerations-ID med maximalt antal händelser
```
PS C:\>Get-AzureRmLog -MaxEvents 100
```

Det här kommandot listar de flesta 100-händelser som är kopplade till användarens prenumerations-ID som tog sju dagar från dagens datum/tid.

### Exempel 3: Hämta en händelse logg efter prenumerations-ID med start tid.
```
PS C:\>Get-AzureRmLog -StartTime 2017-06-01T10:30
```

Det här kommandot listar de flesta 1000-händelser som är kopplade till användarens prenumerations-ID som ägde rum på eller efter 2017 – 06-01T10:30 lokal tid om detta datum/tid inte är äldre än 90 dagar från dagens datum/tid.

### Exempel 4: Hämta en händelse logg efter abonnemangs-ID med start-och slut tid.
```
PS C:\>Get-AzureRmLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

Det här kommandot listar de flesta 1000 av de händelser som är kopplade till användarens prenumerations-ID som ägde rum på eller efter 2017 – 04-01T10:30 lokal tid och tidigare än 2017-04-14T11:30 lokal tid om hela datum-och tidsintervallet inte är äldre än 90 dagar från dagens datum/tid, t. ex.

### Exempel 5: Hämta en händelse logg efter ett korrelations-ID
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

Det här kommandot listar de flesta 1000-händelser som är kopplade till det angivna korrelations-ID: t som ägde sju dagar från dagens datum/tid. 
**Obs!** detta är vanligt vis bara en händelse.

### Exempel 6: Hämta en händelse logg efter ett korrelations-ID med maximalt antal händelser
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxEvents 100
```

Det här kommandot listar de flesta 100-händelser som är kopplade till det angivna korrelations-ID: t som ägde sju dagar från dagens datum/tid. 
**Obs!** detta är vanligt vis bara en händelse.

### Exempel 7: Hämta en händelse logg genom att använda ett korrelations-ID och start tid
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

Det här kommandot listar de flesta 1000-händelser som är kopplade till det angivna korrelations-ID: t som ägde rum på eller efter 2017 – 05-22T04.30:00 lokal tid om start tiden inte är äldre än 90 dagar från dagens datum/tid.
**Obs!** detta är vanligt vis bara en händelse.

### Exempel 8: Hämta en händelse logg efter ett korrelations-ID med start-och slut tid
```
PS C:\>Get-AzureRmLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

Det här kommandot listar de flesta 1000-händelser som är kopplade till det angivna korrelations-ID: t som ägde rum på eller efter 2017 – 04-15T04 = 30 lokal tid, men före 2017-04-25T12:30 lokal tid om hela datum-och tidsintervallet inte är äldre än 90 dagar från dagens datum/tid, t. ex.: bevarande period.

### Exempel 9: Hämta en händelse logg för en resurs grupp
```
PS C:\>Get-AzureRmLog -ResourceGroupName "Contoso-Web-CentralUS"
```

Det här kommandot listar 1000 de händelser som är kopplade till den angivna resurs gruppen som ägde rum 7 dagar från dagens datum/tid.

### Exempel 10: Hämta en händelse logg för en resurs grupp med maximalt antal händelser
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -MaxEvents 100
```

Det här kommandot listar högst 100 händelser kopplade till den angivna resurs gruppen som ägde rum 7 dagar efter det aktuella datumet/tiden.

### Exempel 11: Hämta en händelse logg för en resurs grupp efter start tid
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

Det här kommandot listar högst 1000 evetns associerade med den angivna resurs gruppen som ägde rum på eller efter 2017 – 05-22T04:30:00 lokal tid om start tiden inte är äldre än 90 dagar från dagens datum/tid.

### Exempel 12: Hämta en händelse logg för en resurs grupp med start-och slut tid
```
PS C:\>Get-AzureRmLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Det här kommandot listar de flesta 1000-händelser som är kopplade till den angivna resurs gruppen som ägde rum på eller efter 2017 – 04-15T04:30 lokal tid, men före 2017-04-25T12:30 lokal tid om hela datum-och tidsintervallet inte är äldre än 90 dagar från dagens datum/tid, dvs: bevarande period.

### Exempel 13: Hämta en händelse logg efter resurs-ID
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

Det här kommandot listar de flesta 1000-händelser som är kopplade till angivet resurs-ID som ägde rum 7 dagar från dagens datum/tid.

### Exempel 14: Hämta en händelse logg efter resurs-ID med maximalt antal händelser
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxEvents 100
```

Det här kommandot listar de flesta 100-händelser som är kopplade till angivet resurs-ID som ägde rum 7 dagar från dagens datum/tid.

### Exempel 15: Hämta en händelse logg efter resurs-ID med en start tid
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

Det här kommandot listar de flesta 1000-händelser som är kopplade till angivet resurs-ID som ägde rum på eller efter 2017 – 05-22T04:30:00 lokal tid om start tiden inte är äldre än 90 dagar från dagens datum/tid.

### Exempel 16: Hämta en händelse logg efter resurs-ID med start-och slut tid
```
PS C:\>Get-AzureRmLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Det här kommandot listar de flesta 1000-händelser som är kopplade till angivet resurs-ID som ägde rum på eller efter 2017 – 04-15T04:30 lokal tid, men före 2017-04-25T12:30 lokal tid om hela datum-och tidsintervallet inte är äldre än 90 dagar efter det aktuella datumet/tiden, dvs: bevarande period.

### Exempel 17: Hämta en händelse logg per resurs leverantör
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web"
```

Det här kommandot listar de flesta 1000-händelser som är kopplade till den angivna resurs leverantören som ägde rum 7 dagar från dagens datum/tid.

### Exempel 18: Hämta en händelse logg från en resurs leverantör med maximalt antal händelser
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -MaxEvents 100
```

Det här kommandot listar de flesta 100-händelser som är kopplade till den angivna resurs leverantören som ägde rum 7 dagar från dagens datum/tid.

### Exempel 19: Hämta en händelse logg från en resurs leverantör med en start tid
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

Det här kommandot listar de flesta 1000-händelser som är kopplade till den angivna resurs leverantören som ägde rum på eller efter 2017 – 05-22T04:30:00 lokal tid om start tiden inte är äldre än 90 dagar från dagens datum/tid.

### Exempel 20: Hämta en händelse logg från en resurs leverantör med start-och slut tid
```
PS C:\>Get-AzureRmLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Det här kommandot listar de flesta 1000-händelser som är kopplade till den angivna resurs leverantören som ägde rum på eller efter 2017 – 04-15T04:30 lokal tid, men före 2017-04-25T12:30 lokal tid om hela datum-och tidsintervallet inte är äldre än 90 dagar efter det aktuella datumet/tiden, dvs: bevarande period.

## MALLPARAMETRAR

### -Ringer
Anger en uppringare.

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

### -CorrelationId
Anger korrelations-ID.
Denna parameter är obligatorisk.

```yaml
Type: System.String
Parameter Sets: GetByCorrelationId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DetailedOutput
Anger att den här cmdleten visar detaljerade utdata.
Utdata sammanfattas som standard.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Switch not present = False, i.e. output summarized
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slut tid
Anger slut tiden för frågan i lokal tid.
Standardvärdet är den aktuella tiden.
Värdet måste vara senare än *StartTime*.
Du kan använda Get-Date cmdlet för att hämta ett **datetime** -objekt.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Current date (time: 00:00:00 AM) + 1 day
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxRecord
Anger det totala antalet poster som ska hämtas för det angivna filtret.
Standardvärdet är 1000 och det högsta tillåtna värdet är 100000. Negativa värden och 0 ignoreras och standardvärdet används.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1000
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på resurs gruppen.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Anger resurs-ID.

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceProvider
Anger ett filter efter resurs leverantör.

```yaml
Type: System.String
Parameter Sets: GetByResourceProvider
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartTime
Anger start tiden för frågan i lokal tid.
Standardvärdet är *slut* tid minus sju dagar.
Du kan använda Get-Date cmdlet för att hämta ett **datetime** -objekt.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: EndTime - 7 days
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Status
Anger status.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. Nullable ' 1 [[system. DateTime, mscorlib, version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

### System. String

### System. Management. Automation. SwitchParameter

### System. Int32

## VÄRDEN

### Microsoft. Azure. commands. Insights. OutputClasses. PSEventData

## ANMÄRKNINGAR

## RELATERADE LÄNKAR
