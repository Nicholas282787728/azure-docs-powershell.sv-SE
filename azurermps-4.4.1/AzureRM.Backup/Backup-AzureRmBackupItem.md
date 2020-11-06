---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9FF4F649-F50C-4C27-842F-1CD6C5BC7A2B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
ms.openlocfilehash: 1cb5ccf56a2ef6888231ca81df0e352f5d505e7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574747"
---
# Backup-AzureRmBackupItem

## Sammanfattning
Startar en säkerhets kopiering för en säkerhets kopia.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Backup-AzureRmBackupItem [-Item] <AzureRMBackupItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## PROBLEMBESKRIVNING
**Säkerhets kopiering-AzureRmBackupItem-** cmdleten startar en säkerhets kopiering för ett skyddat Azure Backup-objekt som inte är bundet till säkerhets kopierings schema.
Du kan utföra den första säkerhets kopieringen direkt efter att du har aktiverat skyddet eller starta en säkerhets kopiering efter en schemalagd säkerhets kopiering.

Om det finns ett befintligt säkerhets kopierings jobb Miss lyckas denna cmdlet.

## BESKRIVS

### Exempel 1: börja säkerhetskopiera en virtuell dator
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container | Backup-AzureRmBackupItem
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
```

Det första kommandot får valvet med namnet Vault03 med hjälp av Get-AzureRmBackupVault cmdlet.
Kommandot lagrar objektet i $Vault variabel.

Det andra kommandot får en behållare som har det angivna namnet i valvet i $Vault genom att använda Get-AzureRmBackupContainer cmdlet.
Kommandot lagrar objektet i $Container variabel.

Med det senaste kommandot hämtas säkerhets kopierings objekt i $Container med hjälp av Get-AzureRmBackupItem cmdlet.
Kommandot skickar objekten till den aktuella cmdleten med hjälp av pipeline-operatorn.
Den aktuella cmdleten börjar säkerhetskopiera den virtuella datorn i behållaren.

## MALLPARAMETRAR

### -Objekt
Anger ett säkerhets kopierings objekt som denna cmdlet startar en säkerhets kopierings åtgärd för.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### AzureRMBackupItem

## VÄRDEN

### AzureRmBackupJob

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmBackupItem](./Get-AzureRmBackupItem.md)

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Återställ-AzureRmBackupItem](./Restore-AzureRmBackupItem.md)


