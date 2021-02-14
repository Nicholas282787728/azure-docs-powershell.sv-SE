---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: 9b57d7584ee7720ec73aa57ddec070ad26ddff9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221463"
---
# Get-AzActivityLog

## SYNOPSIS
Hämta aktivitetslogghändelser.

## SYNTAX

### GetByCorrelationId
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceId
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceGroup
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceProvider
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetBySubscription
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdlet Get-AzActivityLog hämta aktivitetslogghändelser. Händelserna kan associeras med aktuellt prenumerations-ID, korrelations-ID, resursgrupp, resurs-ID eller resursleverantör.

## EXEMPEL

### Exempel 1: Hämta en händelselogg med prenumerations-ID
```
PS C:\>Get-ActivityAzLog
```

Det här kommandot visar som mest 1 000 händelser som är associerade med användarens prenumerations-ID som ägde rum 7 dagar från dagens datum/tid.

### Exempel 2: Hämta en händelselogg med prenumerations-ID med maximalt antal händelser
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

Det här kommandot listar som mest 100 händelser som är associerade med användarens prenumerations-ID som ägde rum 7 dagar från dagens datum/tid.

### Exempel 3: Hämta en händelselogg med prenumerations-ID med en starttid.
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

Det här kommandot visar som mest 1 000 händelser som är associerade med användarens prenumerations-ID som ägde rum på eller efter 2017-06-01T10:30 lokal tid om datumet/tiden inte är äldre än 90 dagar från aktuellt datum/tid.

### Exempel 4: Hämta en händelselogg med prenumerations-ID med starttid och sluttid.
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

Med det här kommandot visas som mest 1 000 händelser som är associerade med användarens prenumerations-ID som ägde rum på eller efter 2017-04-01T10:30 lokal tid och före 2017-04-14T11:30 lokal tid om hela datum-/tidsintervallet inte är äldre än 90 dagar från aktuellt datum/tid, dvs. kvarhållningsperioden.

### Exempel 5: Hämta en händelselogg med korrelations-ID
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

Med det här kommandot visas som mest 1 000 händelser som är associerade med det angivna korrelations-ID:t som ägde rum 7 dagar från aktuellt datum/tid. 
**OBS!** Det här är vanligtvis bara en händelse.

### Exempel 6: Hämta en händelselogg med korrelations-ID med maximalt antal händelser
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

Det här kommandot visar som mest 100 händelser som är associerade med det angivna korrelations-ID:t som ägde rum 7 dagar från dagens datum/tid. 
**OBS!** Det här är vanligtvis bara en händelse.

### Exempel 7: Hämta en händelselogg med korrelations-ID och starttid
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

Med det här kommandot visas som mest 1 000 händelser som är associerade med det angivna korrelations-ID:t som ägde rum på eller efter 2017-05-22T04:30:00 lokal tid om starttiden inte är äldre än 90 dagar från aktuellt datum/tid.
**OBS!** Det här är vanligtvis bara en händelse.

### Exempel 8: Hämta en händelselogg med korrelations-ID med starttid och sluttid
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

Med det här kommandot visas som mest 1 000 händelser som är associerade med det angivna korrelations-ID:t som ägde rum på eller efter 2017-04-15T04:30 lokal tid, men före 2017-04-25T12:30 lokal tid om hela datum-/tidsintervallet inte är äldre än 90 dagar från aktuellt datum/tid, det vill säga lagringstiden.

### Exempel 9: Hämta en händelselogg för en resursgrupp
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

Med det här kommandot visas som mest 1 000 händelser som är associerade med den angivna resursgruppen som ägde rum 7 dagar från dagens datum/tid.

### Exempel 10: Hämta en händelselogg för en resursgrupp med maximalt antal händelser
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

Det här kommandot listar som mest 100 händelser som är associerade med den angivna resursgruppen som ägde rum 7 dagar från dagens datum/tid.

### Exempel 11: Hämta en händelselogg för en resursgrupp efter starttid
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

Med det här kommandot visas som mest 1 000 händelser som är associerade med den angivna resursgruppen som ägde rum på eller efter 2017-05-22T04:30:00 lokal tid om starttiden inte är äldre än 90 dagar från aktuellt datum/tid.

### Exempel 12: Hämta en händelselogg för en resursgrupp med starttid och sluttid
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Med det här kommandot visas som mest 1 000 händelser som är associerade med den angivna resursgruppen som ägde rum på eller efter 2017-04-15T04:30 lokal tid, men före 2017-04-25T12:30 lokal tid om hela datum/tidintervall inte är äldre än 90 dagar från aktuellt datum/tid, det vill säga lagringstiden.

### Exempel 13: Hämta en händelselogg med resurs-ID
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

Med det här kommandot visas som mest 1 000 händelser som är associerade med det angivna resurs-ID:t som ägde rum 7 dagar från dagens datum/tid.

### Exempel 14: Hämta en händelselogg med resurs-ID med maximalt antal händelser
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

Med det här kommandot visas som mest 100 händelser som är associerade med det angivna resurs-ID:t som ägde rum 7 dagar från dagens datum/tid.

### Exempel 15: Hämta en händelselogg med resurs-ID med en starttid
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

Med det här kommandot visas som mest 1 000 händelser som är associerade med det angivna resurs-ID som ägde rum på eller efter 2017-05-22T04:30:00 lokal tid om starttiden inte är äldre än 90 dagar från aktuellt datum/tid.

### Exempel 16: Hämta en händelselogg med resurs-ID med en starttid och sluttid
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Med det här kommandot visas som mest 1 000 händelser som är associerade med det angivna resurs-ID som ägde rum på eller efter 2017-04-15T04:30 lokal tid, men före 2017-04-25T12:30 lokal tid om hela datum/tidsintervall inte är äldre än 90 dagar från aktuellt datum/tid, det vill säga bevarandetiden.

### Exempel 17: Hämta en händelselogg av resursleverantören
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

Det här kommandot listar som mest 1 000 händelser som är associerade med den angivna resursleverantören som ägde rum 7 dagar från dagens datum/tid.

### Exempel 18: Hämta en händelselogg av resursleverantören med maximalt antal händelser
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

Det här kommandot listar som mest 100 händelser som är associerade med den angivna resursleverantören som ägde rum 7 dagar från dagens datum/tid.

### Exempel 19: Hämta en händelselogg av resursleverantören med en starttid
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

Det här kommandot listar som mest 1 000 händelser som är associerade med den angivna resursleverantören som ägde rum på eller efter 2017-05-22T04:30:00 lokal tid om starttiden inte är äldre än 90 dagar från aktuellt datum/tid.

### Exempel 20: Hämta en händelselogg av resursleverantören med en starttid och sluttid
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Med det här kommandot visas som mest 1 000 händelser som är associerade med den angivna resursleverantören som ägde rum på eller efter 2017-04-15T04:30 lokal tid, men före 2017-04-25T12:30 lokal tid om hela datum-/tidsintervallet inte är äldre än 90 dagar från aktuellt datum/tid, det vill säga lagringsperioden.

## PARAMETERS

### -Uppringare
Uppringare av händelser att hämta

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
The CorrelationId

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
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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

### -DetailedOutput
Returnera objekt med all information om händelserna (standardinställningen är att endast returnera vissa attribut, det vill säga inga detaljer)

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EndTime
Frågesluttiden

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxRecord
Maximalt antal poster att hämta.
Alias: MaxRecords, MaxEvents

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Resursgruppnamnet

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
Resurs-ID

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
Namnet ResourceProvider

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
Korrelations-ID:t för frågan

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Status
Status för händelser att hämta

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.String

### System.Management.Automation.SwitchParameter

### System.Int32

## UTDATA

### Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData

## ANTECKNINGAR

## RELATERADE LÄNKAR
