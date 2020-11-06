---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 44C5AF58-ADC1-4BC6-9771-3FD8F0480106
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
ms.openlocfilehash: d502596b8c5ddde576b5fd22ee31398b2c4e869a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584808"
---
# Stop-AzureRmBackupJob

## Sammanfattning
Avbryter ett befintligt säkerhets kopierings jobb.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### IdFiltersSet
```
Stop-AzureRmBackupJob -Vault <AzureRMBackupVault> -JobID <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### JobFiltersSet
```
Stop-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Stop-AzureRmBackupJob** avbryter ett befintligt Azure Backup-jobb.
Använd den här parametern för att stoppa ett jobb som tar för lång tid att blockera andra aktiviteter.

Du kan bara avbryta följande typer av jobb: 

- Reservdomänkontrollant
- Terställa

## BESKRIVS

### Exempel 1: stoppa ett säkerhets kopierings jobb med ett jobb-ID
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Job = Get-AzureRmBackupJob -Vault $Vault -Operation Backup
PS C:\> Stop-AzureRmBackupJob -Vault $Vault -JobID $Job.InstanceId
```

Det första kommandot får valvet med namnet Vault03 med hjälp av cmdleten **Get-AzureRmBackupVault** .
Kommandot lagrar objektet i $Vault variabel.

Det andra kommandot får ett säkerhets kopierings jobb från valvet i $Vault genom att använda cmdleten **Get-AzureRmBackupJob** .
Kommandot lagrar jobbet i $Job variabel.
I det här exemplet finns det bara en säkerhets kopierings åtgärd i det angivna valvet.

Det sista kommandot stoppar det jobb som har angivet ID.

### Exempel 2: stoppa alla återställnings åtgärder
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Operation Restore | Stop-AzureRmBackupJob
```

Det här kommandot får alla återställnings operationer i valvet i $Vault och överför dem sedan till den aktuella cmdleten med hjälp av pipeline-operatorn.
Den aktuella cmdleten stoppar varje jobb.

## MALLPARAMETRAR

### -Jobb
Anger ett jobb som denna cmdlet avbryter.
Använd Get-AzureRmBackupJob cmdlet för att få ett **AzureRmBackupJob** -objekt.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobID
Anger ett jobb som denna cmdlet avbryter.
Använd Get-AzureRmBackupJob cmdlet för att få ett **AzureRmBackupJob** -objekt.

```yaml
Type: System.String
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Valv
Anger det säkerhets kopierings valv där denna cmdlet avbryter ett jobb.
Använd Get-AzureRmBackupVault cmdlet för att få ett **AzureRmBackupVault** -objekt.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
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

### Ingen

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmBackupJob](./Get-AzureRmBackupJob.md)

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Wait-AzureRmBackupJob](./Wait-AzureRmBackupJob.md)


