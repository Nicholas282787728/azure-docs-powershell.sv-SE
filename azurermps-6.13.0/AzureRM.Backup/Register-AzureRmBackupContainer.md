---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 394500DB-D2BB-4793-8D9F-2CAF4D892A55
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/register-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
ms.openlocfilehash: 3431650296c29f06131f946910d1cbc3dc6e6bb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755552"
---
# Register-AzureRmBackupContainer

## Sammanfattning
Registrerar behållaren med ett säkerhets kopierings valv.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### V1VM
```
Register-AzureRmBackupContainer -Name <String> -ServiceName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### V2VM
```
Register-AzureRmBackupContainer -Name <String> -ResourceGroupName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
**Register-AzureRmBackupContainer** cmdlet registrerar behållaren med ett Azure Backup-valv.
Om du vill konfigurera säkerhets kopiering med Azure Backup måste du först registrera din server eller virtuella dator med ett säkerhets kopierings valv.
Denna cmdlet registrerar en infrastruktur som en tjänst (IaaS) med det angivna valvet.
Registrerings åtgärden associerar den virtuella Azure-datorn med säkerhets kopierings valvet och spårar den virtuella datorn genom säkerhets kopierings cykeln.

## BESKRIVS

### Exempel 1: registrera en virtuell dator i ett säkerhets kopierings valv
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Register-AzureRmBackupContainer -Vault $Vault -Name "Contoso03Vm" -ServiceName "ContosoService27"
```

Det första kommandot får valvet med namnet Vault03 med hjälp av Get-AzureRmBackupVault cmdlet.
Kommandot lagrar valvet i $Vault variabel.
Det andra kommandot registrerar den virtuella datorn med namnet Contoso03Vm med valvet i $Vault.
Den virtuella datorn tillhör tjänsten ContosoService27.

## MALLPARAMETRAR

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure

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

### -Namn
Anger namnet på den virtuella dator som denna cmdlet registrerar.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på resurs gruppen för den virtuella datorn.

```yaml
Type: System.String
Parameter Sets: V2VM
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Anger tjänst namnet på den virtuella dator som denna cmdlet registrerar.
Vanligt vis har ett moln tjänst namn ett suffix. cloudapp.net.
Ta inte med suffixet när du anger den här parametern.
Använd Get-AzureRMVM cmdlet för att få information om en virtuell dator.
Tjänstens namn är egenskapen **DeploymentName** för den virtuella datorns objekt.

```yaml
Type: System.String
Parameter Sets: V1VM
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Valv
Anger det säkerhets kopierings valv som denna cmdlet registrerar virtuell dator med.
Använd Get-AzureRmBackupVault cmdlet för att få ett **AzureRmBackupVault** -objekt.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### System. String

### Microsoft. Azure. commands. AzureBackup. Models. AzureRMBackupVault
Parametrar: valv (ByValue)

## VÄRDEN

### Microsoft. Azure. commands. AzureBackup. Models. AzureRMBackupJob

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)


