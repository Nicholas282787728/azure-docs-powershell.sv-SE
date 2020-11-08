---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: 81c1aeded9b4bb40998448d61a5edbf35742bfcc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088613"
---
# Get-AzRecoveryServicesBackupJobDetail

## Sammanfattning

Hämtar information om ett säkerhets kopierings jobb.

## FRÅGESYNTAXEN

### JobFilterSet (standard)
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### IdFilterSet
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING

Cmdleten **Get-AzRecoveryServicesBackupJobDetail** hämtar information om Azure Backup-jobbet för ett angivet jobb.
Ange valv kontexten med parametern-VaultId.

Varning: **Get-AzRecoveryServicesBackupJobDetails** -alias tas bort i en fortsättnings ändring.

## BESKRIVS

### Exempel 1: Hämta information om jobb för misslyckade jobb

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

Det första kommandot får en matris med misslyckade jobb i valvet och lagrar dem i $Jobs matrisen.
Det andra kommandot får jobb informationen för misslyckade jobb i $Jobs och lagrar dem sedan i $JobDetails variabel.
Det sista kommandot visar fel information för misslyckade jobb.

## MALLPARAMETRAR

### -DefaultProfile

Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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

### -Jobb

Anger vilket jobb som ska erhållas.
Om du vill hämta ett **BackupJob** -objekt använder du cmdleten **Get-AzRecoveryServicesBackupJob** .

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: JobFilterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId

Anger ID för ett säkerhets kopierings jobb.
ID är egenskapen JobId för en **Microsoft. Azure.-kommandon. RecoveryServices. backup. cmdletar. Models. JobBase** -objekt.

```yaml
Type: System.String
Parameter Sets: IdFilterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultId

ARM-ID för Recovery Services-valvet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### System. String

## VÄRDEN

### Microsoft. Azure. kommando. RecoveryServices. backup. cmdletar. Models. JobBase

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzRecoveryServicesBackupJob](./Get-AzRecoveryServicesBackupJob.md)
