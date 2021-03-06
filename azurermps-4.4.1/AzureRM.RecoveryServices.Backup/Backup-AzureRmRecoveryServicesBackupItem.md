---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: acf448b58fdf7bcc218ece8b5fb2415bc30981ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756894"
---
# Backup-AzureRmRecoveryServicesBackupItem

## Sammanfattning
Startar en säkerhets kopiering för en säkerhets kopia.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Backup-AzureRmRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
**Säkerhets kopiering-AzureRmRecoveryServicesBackupItem-** cmdleten startar en säkerhets kopiering för ett skyddat Azure Backup-objekt som inte är bundet till säkerhets kopierings schema.
Du kan utföra den första säkerhets kopieringen direkt efter att du har aktiverat skyddet eller starta en säkerhets kopiering efter en schemalagd säkerhets kopiering.

Ställ in valv kontexten med hjälp av Set-AzureRmRecoveryServicesVaultContext cmdlet innan du använder den aktuella cmdleten.

## BESKRIVS

### Exempel 1: starta en säkerhets kopia av ett säkerhets kopie objekt
```
PS C:\> $NamedContainer = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "pstestv2vm1" 
PS C:\> $Item = Get-AzureRmRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM 
PS C:\> $Job = Backup-AzureRmRecoveryServicesItem -Item $Item
Operation        Status               StartTime            EndTime                   JOBID                           
------------     ---------            ------               ---------                 -------                                         
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

Det första kommandot får säkerhets kopierings behållaren av typen AzureVM med namnet pstestv2vm1 och lagrar den sedan i $NamedContainer variabel.

Det andra kommandot får det säkerhets kopie objekt som motsvarar behållaren i $NamedContainer och lagrar det sedan i $Item-variabeln.

Det sista kommandot utlöser säkerhets kopierings jobbet i $Item.

## MALLPARAMETRAR

### -ExpiryDateTimeUTC
Anger en förfallo tid som ett **datetime** -objekt.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Objekt
Anger ett säkerhets kopierings objekt som denna cmdlet startar en säkerhets kopierings åtgärd för.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
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

### DateTime
Parametern ' ExpiryDateTimeUTC ' godkänner värdet för typen ' DateTime ' från pipeline

### ItemBase
Parametern ' item ' godkänner värdet av typen ' ItemBase ' från pipeline

## VÄRDEN

### Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmRecoveryServicesBackupContainer](./Get-AzureRmRecoveryServicesBackupContainer.md)

[Get-AzureRmRecoveryServicesBackupItem](./Get-AzureRmRecoveryServicesBackupItem.md)

[Återställ-AzureRmRecoveryServicesBackupItem](./Restore-AzureRmRecoveryServicesBackupItem.md)


