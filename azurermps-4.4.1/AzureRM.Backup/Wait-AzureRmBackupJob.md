---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: C5126E20-0A93-4ACE-8297-F1E8E17BEF53
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
ms.openlocfilehash: 6ee1319881b200b3fcae56e433f81460bfc90274
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583371"
---
# Wait-AzureRmBackupJob

## Sammanfattning
Väntar på att ett säkerhets kopierings jobb ska slutföras.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Wait-AzureRmBackupJob -Job <Object> [-TimeOut <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **wait-AzureRmBackupJob** väntar på att ett Azure Backup-jobb ska avslutas.
Det kan ta lång tid att säkerhetskopiera jobb.
Om du kör ett säkerhets kopierings jobb som en del av ett skript kanske du vill tvinga skriptet att vänta på jobbet innan det fortsätter med andra aktiviteter.

Ett skript som innehåller denna cmdlet kan vara enklare än en som Avsök säkerhets kopierings tjänsten för jobb statusen.

## BESKRIVS

## MALLPARAMETRAR

### -Jobb
Anger ett jobb som denna cmdlet avbryter.
Använd Get-AzureRmBackupJob cmdlet för att få ett **AzureRmBackupJob** -objekt.

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TimeOut
Anger den maximala tiden i sekunder som denna cmdlet väntar på att jobbet ska avslutas.
Vi rekommenderar att du anger ett timeout-värde.

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### AzureRmBackupJob

## VÄRDEN

### AzureRmBackupJob[]

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmBackupJob](./Get-AzureRmBackupJob.md)

[Stopp-AzureRmBackupJob](./Stop-AzureRmBackupJob.md)


