---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CF3548F6-03FE-44D6-AA2C-1015611C657A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0423fe51a047385ef6395075dd116b4d4189c667
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093278"
---
# Get-AzureStorSimpleTask

## Sammanfattning
Status för en aktivitet på en StorSimple-enhet.

## FRÅGESYNTAXEN

```
Get-AzureStorSimpleTask -InstanceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureStorSimpleTask** returnerar statusen för en aktivitet som körs asynkront på en Azure StorSimple-enhet.

När du hanterar en StorSimple-enhet kan de flesta åtgärder för att skapa, läsa, uppdatera och ta bort vara asynkront.
Windows PowerShell returnerar en **TaskId**.
Använd ID för att få aktivitetens aktuella status.

## BESKRIVS

### Exempel 1: få statusen för en uppgift
```
PS C:\>Get-AzureStorSimpleTask -TaskId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: d9c1e8a7-994f-4698-8b42-064600b45cad_PS
VERBOSE: ClientRequestId: aae17c82-6fd3-435e-a965-1c66b3c955fe_PS


AsyncTaskAggregatedResult : Succeeded
Error                     : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
Result                    : Succeeded
Status                    : Completed
TaskId                    : 53816d8d-a8b5-4c1d-a177-e59007608d6d
TaskSteps                 : {}
StatusCode                : OK
RequestId                 : e9174990825750bba69383748f23019c
```

Det här kommandot får statusen för den aktivitet som har angivet ID.
Resultatet visar att aktiviteten har statusen slutförd och att resultatet lyckades.

## MALLPARAMETRAR

### -InstanceId
Anger ID för den aktivitet som cmdleten ska spåra status för.

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskId

Required: True
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

### Ingen

## VÄRDEN

### JobStatusInfo
Denna cmdlet returnerar ett **TaskStatusInfo** -objekt som innehåller följande fält: 

- **Fel**.
**ErrorDetails** , som innehåller **kod** och **meddelande**.
- **TaskId**.
**Sträng**.
ID för den uppgift vars status returneras.
- **TaskSteps**.
**Ilist \<TaskStep\>**.
Varje **TaskStep** -objekt innehåller **detaljerad** , **ErrorCode** , **meddelande** , **resultat** och **status**.
- **Resultat**.
**TaskResult** , som innehåller aktivitetens övergripande resultat.
Giltiga värden är: misslyckades, lyckades, PartialSuccess, annullerade och ogiltiga.
- **Status**.
**TaskStatus** , som innehåller aktivitetens övergripande kör status.
Giltiga värden är: InProgress, ogiltigt och slutfört.
- **TaskResult**.
**TaskResult** , ett värde som beräknas baserat på **resultat** och **status**.
Giltiga värden är: misslyckad, lyckad, pågående, PartialSuccess, avbruten och ogiltig.

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

