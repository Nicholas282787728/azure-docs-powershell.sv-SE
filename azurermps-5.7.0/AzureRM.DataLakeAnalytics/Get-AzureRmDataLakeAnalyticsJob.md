---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: ca480d266f4ab7706841fb901fa714dbe632ec2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573446"
---
# Get-AzureRmDataLakeAnalyticsJob

## Sammanfattning
Hämtar ett data Lake Analytics-jobb.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### GetAllInResourceGroupAndAccount (standard)
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetBySpecificJobInformation
```
Get-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmDataLakeAnalyticsJob** får ett Azure Data Lake Analytics-jobb.
Om du inte anger något jobb får denna cmdlet alla jobb.

## BESKRIVS

### Exempel 1: Hämta ett angivet jobb
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

Det här kommandot får jobbet med angivet ID.

### Exempel 2: få jobb skickade under den senaste veckan
```
PS C:\>Get-AzureRmDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

Med det här kommandot hämtas jobb som skickas under den senaste veckan.

## MALLPARAMETRAR

### -Konto
Anger namnet på ett data Lake Analytics-konto.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inkludera
Anger alternativ som anger vilken typ av ytterligare information som ska hämtas om jobbet.
De acceptabla värdena för den här parametern är:

- Ingen
- DebugInfo
- Statistik
- Alla

```yaml
Type: ExtendedJobData
Parameter Sets: GetBySpecificJobInformation
Aliases: 
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobId
Anger ID för det jobb som ska visas.

```yaml
Type: Guid
Parameter Sets: GetBySpecificJobInformation
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Namn
Anger ett namn som ska användas för att filtrera jobb listans resultat.
De acceptabla värdena för den här parametern är:

- Ingen
- DebugInfo
- Statistik
- Alla

```yaml
Type: String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PipelineId
Ett valfritt ID som endast anger jobb delar av den angivna pipeline ska returneras.

```yaml
Type: Guid
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecurrenceId
Ett valfritt ID som endast anger att jobb delar av den angivna upprepningen ska returneras.

```yaml
Type: Guid
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Resultat
Anger ett resultat filter för jobb resultaten.
De acceptabla värdena för den här parametern är:

- Ingen
- Annullerats
- Startade
- Utför

```yaml
Type: JobResult[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -State
Anger ett status filter för jobb resultaten.
De acceptabla värdena för den här parametern är:

- Allmänt
- Nya
- Kompilera
- Scheman
- I kö
- Sidnumrering
- Pausad
- Aktiv
- Avslutade

```yaml
Type: JobState[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubmittedAfter
Anger ett datum filter.
Använd den här parametern för att filtrera jobb resultaten till jobb som har inlämnats efter det angivna datumet.

```yaml
Type: DateTimeOffset
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubmittedBefore
Anger ett datum filter.
Använd den här parametern för att filtrera jobb resultaten till jobb som skickas före angivet datum.

```yaml
Type: DateTimeOffset
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sändning
Anger e-postadressen för en användare.
Använd den här parametern för att filtrera jobb listans resultat till jobb som skickas av en viss användare.

```yaml
Type: String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Överst
Ett valfritt värde som anger hur många jobb som ska returneras. Standardvärdet är 500

```yaml
Type: Int32
Parameter Sets: GetAllInResourceGroupAndAccount
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

### Ande
Parametern ' JobId ' godkänner värdet av typen ' GUID ' från pipeline

## VÄRDEN

### JobInformation
Den angivna jobb informations informationen

### Förteckning<PSJobInformationBasic>
Listan med jobb i angivet data Lake Analytics-konto.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Stopp-AzureRmDataLakeAnalyticsJob](./Stop-AzureRmDataLakeAnalyticsJob.md)

[Skicka-AzureRmDataLakeAnalyticsJob](./Submit-AzureRmDataLakeAnalyticsJob.md)

[Wait-AzureRmDataLakeAnalyticsJob](./Wait-AzureRmDataLakeAnalyticsJob.md)


