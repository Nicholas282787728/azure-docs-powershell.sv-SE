---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 2605B232-10CA-4426-9917-7C9719C15166
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/enable-azurermbackupcontainerreregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
ms.openlocfilehash: f64453995418df572480426e7c2c63e497cf000f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582100"
---
# Enable-AzureRmBackupContainerReregistration

## Sammanfattning
Registrerar en server för att ansluta till ett säkerhets kopierings valv.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Enable-AzureRmBackupContainerReregistration [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Enable-AzureRmBackupContainerReregistration** registrerar en server för att ansluta till ett Azure Backup-valv och fortsätter med plats kedjan för säkerhets kopiering.

Om du förstör en server kvarstår alla dess säkerhets kopierings punkter i säkerhets kopierings valvet.
Om du skapar en ersättnings Server och tilldelar den samma fullkvalificerade domän namn kan du koppla tillbaka servern till samma valv.
Med den här cmdleten kan du göra säkerhets kopior och lägga till nya säkerhets kopior i den befintliga uppsättningen.
Den nya servern fortsätter i säkerhets kopierings kedjan.

## BESKRIVS

## MALLPARAMETRAR

### -Container
Anger den behållare som den här cmdleten registrerar.
För att få en **AzureRmBackupContainer** , Använd cmdleten Get-AzureRmBackupContainer.

```yaml
Type: AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### AzureBackupContainer

## VÄRDEN

### Ingen

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[Register-AzureRmBackupContainer](./Register-AzureRmBackupContainer.md)


