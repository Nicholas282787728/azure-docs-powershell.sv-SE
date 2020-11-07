---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 95FF3F7A-5CC6-4AA6-A393-5EBB5579D9A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
ms.openlocfilehash: 18383ffeb35b1ce6bb2651be041e07b6164e55da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757722"
---
# Get-AzureRmBackupVault

## Sammanfattning
Hämtar säkerhets kopierings valv.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmBackupVault [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmBackupVault** får Azure Backup-valv.
Denna cmdlet returnerar **AzureRmBackupVault** -objekt som ska användas med andra cmdletar.

## BESKRIVS

### Exempel 1: Visa alla säkerhets kopierings valv
```
PS C:\>Get-AzureRmBackupVault
```

Det här kommandot får alla Azure Backup-valv.

### Exempel 2: Visa alla valv som skapats i västra USA
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Region -eq "westus" }
```

Det här kommandot får alla säkerhets kopierings valv.
Kommandot skickar dem till Where-Object cmdlet genom att använda pipeline-operatorn.
Denna cmdlet filtrerar resultaten baserat på egenskapen **område** .
Om du vill ha mer information skriver du `Get-Help Where-Object` .

### Exempel 3: skaffa ett visst valv
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup011/providers/Microsoft.Backup
                    /BackupVault/Vault
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

Det här kommandot får valvet med namnet Vault03.

### Exempel 4: räkna antalet valv som har lokalt redundant lagrings utrymme
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Storage -match "LocallyRedundant" } | Measure-Object
Count    : 4
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property :
```

Det här kommandot får alla Azure Backup-valv.
Kommandot skickar dem till **WHERE-objekt** , som filtrerar resultaten baserat på egenskapen **lagring** .
Kommandot skickar de som har värdet LocallyRedundant till cmdleten Measure-Object och räknar resultatet.
Om du vill ha mer information skriver du `Get-Help Measure-Object` .

## MALLPARAMETRAR

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

### -Namn
Anger namnet på det säkerhets kopierings valv som denna cmdlet får.
Om det finns fler än ett säkerhets kopierings valv med samma namn, returnerar denna cmdlet alla.
Ange parametern *ResourceGroupName* för att få ett unikt valv.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på en Azure-adressresurs där denna cmdlet får ett säkerhets kopierings valv.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### AzureRmBackupVault

## ANMÄRKNINGAR
* Ingen

## RELATERADE LÄNKAR

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[New-AzureRmBackupVault](./New-AzureRmBackupVault.md)

[Remove-AzureRmBackupVault](./Remove-AzureRmBackupVault.md)

[Set-AzureRmBackupVault](./Set-AzureRmBackupVault.md)


