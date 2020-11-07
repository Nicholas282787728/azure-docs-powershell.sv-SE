---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 922BEA08-6619-4D4C-86EC-58279C9E1D93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/unregister-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
ms.openlocfilehash: 059db3658f97a28bda8960384aef4300595dca20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758339"
---
# Unregister-AzureRmBackupContainer

## Sammanfattning
Avregistrerar en behållare från ett säkerhets kopierings valv.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Unregister-AzureRmBackupContainer [-Force] [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Med cmdleten **Unregistered-AzureRmBackupContainer** avregistrerar du den virtuella Windows-servern eller Azure-datorn från ett Azure Backup-valv.
Denna cmdlet tar bort referenser till en behållare från säkerhets kopierings valvet.
Innan du kan avregistrera en behållare måste du ta bort alla skyddade data som är kopplade till den behållaren.

## BESKRIVS

### Exempel 1: avregistrera en Windows Server
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type Windows -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmBackupContainer -Container $Container[0]
Unregister Server
This operation will delete all data in the backup vault that is associated with the server. Are you sure you want to unregister the server? 
[] Yes  [] No  [?] Help (default is "No"): Yes
```

Det första kommandot får valvet med namnet Vault03 med hjälp av Get-AzureRmBackupVault cmdlet.
Kommandot lagrar objektet i $Vault variabel.

Det andra kommandot får en behållare som har det angivna namnet i valvet i $Vault genom att använda Get-AzureRmBackupContainer cmdlet.
Kommandot lagrar objektet i $Container variabel.

Det sista kommandot avregistrerar den angivna Windows-servern från Azure Backup-valvet.

### Exempel 2: avregistrera en Windows Server utan bekräftelse
```
PS C:\>Unregister-AzureRmBackupContainer -Container $Container[0] -Force
```

Det här kommandot avregistrerar den angivna Windows-servern från Azure Backup-valvet, på samma sätt som i det första exemplet.
Det här kommandot anger parametern *Force* .
Därför uppmanas du inte att bekräfta.

## MALLPARAMETRAR

### -Container
Anger den virtuella Windows Server-eller Azure-dator som denna cmdlet avregistrerar.
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

### -Force
Tvingar kommandot att köras utan att fråga efter bekräftelse.
Den här parametern är endast relevant för **AzureBackupContainer** -objekt i Windows.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bekräfta
Du uppmanas att bekräfta innan du kör cmdleten.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som händer om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### AzureBackupContainer

## VÄRDEN

### AzureBackupJob
Denna cmdlet returnerar $Null om behållar typen är Windows Server.

## ANMÄRKNINGAR
* Ingen

## RELATERADE LÄNKAR

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Register-AzureRmBackupContainer](./Register-AzureRmBackupContainer.md)


