---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 8B10E476-F283-4BDC-BFAD-A33F8EC38341
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 9bb6475f0e9ea688c9339980c1a8955ea011fbb7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754314"
---
# Set-AzDataLakeAnalyticsAccount

## Sammanfattning
Ändrar ett data Lake Analytics-konto.

## FRÅGESYNTAXEN

```
Set-AzDataLakeAnalyticsAccount [-Name] <String> [[-Tag] <Hashtable>] [[-ResourceGroupName] <String>]
 [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>] [-QueryStoreRetention <Int32>] [-Tier <TierType>]
 [-FirewallState <FirewallState>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzDataLakeAnalyticsAccount** ändrar ett Azure Data Lake Analytics-konto.

## BESKRIVS

### Exempel 1: ändra data källan för ett konto
```
PS C:\>Set-AzDataLakeAnalyticsAccount -Name "ContosoAdlAcct" -DefaultDataLakeStore "ContosoAdlStore01" -Tags @{"stage"="production"}
```

Det här kommandot ändrar standard data källan och egenskapen Tags för kontot.

## MALLPARAMETRAR

### -AllowAzureIpState
Tillåt/blockera Azure med IP-adresser via brand väggen.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

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

### -FirewallState
Aktivera/inaktivera befintliga brand Väggs regler.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.FirewallState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxAnalyticsUnits
Det valfria Max antalet analys enheter som du kan använda för att uppdatera kontot.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxJobCount
Det valfria högsta tillåtna antalet jobb som körs under kontot samtidigt som du anger.

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

### -Namn
Anger namnet på data Lake Analytics-kontot.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -QueryStoreRetention
Det valfria antalet dagar som jobbets metadata bevaras i kontot.

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

### -ResourceGroupName
Anger namnet på resurs gruppen för data Lake Analytics-kontot.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tagg
En sträng, en sträng ord lista med taggar som är associerade till det här kontot och som ska ersätta den aktuella uppsättningen Taggar

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tier
Önskad åtagande nivå för det här kontot.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

### System. Collections. hash

### System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]

### System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Analytics. Models. TierType, Microsoft. Azure. Management. DataLake. Analytics, version = 3.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]

### System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Analytics. Models. FirewallState, Microsoft. Azure. Management. DataLake. Analytics, version = 3.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]

### System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Analytics. Models. FirewallAllowAzureIpsState, Microsoft. Azure. Management. DataLake. Analytics, version = 3.0.0.0, Culture = neutralt, PublicKeyToken = 31bf3856ad364e35]]

## VÄRDEN

### Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzDataLakeAnalyticsAccount](./Get-AzDataLakeAnalyticsAccount.md)

[New-AzDataLakeAnalyticsAccount](./New-AzDataLakeAnalyticsAccount.md)

[Remove-AzDataLakeAnalyticsAccount](./Remove-AzDataLakeAnalyticsAccount.md)

[Test-AzDataLakeAnalyticsAccount](./Test-AzDataLakeAnalyticsAccount.md)


