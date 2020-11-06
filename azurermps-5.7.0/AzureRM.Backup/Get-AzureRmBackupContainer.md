---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: F3774658-A5E4-40BE-9A85-B33C70BC0A09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
ms.openlocfilehash: abc4bce43c5be267e736cb93e03806cdd802fcb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574439"
---
# Get-AzureRmBackupContainer

## Sammanfattning
Hämtar säkerhets kopierings behållare.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

```
Get-AzureRmBackupContainer [-Name <String>] -Type <AzureBackupContainerType>
 [-ManagedResourceGroupName <String>] [-Status <AzureBackupContainerRegistrationStatus>]
 [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmBackupContainer** får Azure Backup-behållare.

En **AzureBackupContainer** kapslar in data källor, skyddade objekt och återställnings punkter.
En **AzureBackupContainer** kan vara något av följande: 

- En Windows Server-dator
- En System Center Data Protection Manager (SCDPM)-Server 
- En Azure-infrastruktur som tjänst (IaaS)

Innan säkerhets kopiering kan säkerhetskopiera en data källa eller ett objekt måste du registrera den behållare som innehåller den med Azure Backup-tjänsten.
Behållaren måste autentiseras för att skicka säkerhets kopior till säkerhets kopierings valvet.
För Windows Server-datorer och SCDPM-servrar hålls registreringen med det fullt kvalificerade domän namnet för servern.

## BESKRIVS

### Exempel 1: Visa alla servrar registrerade i ett valv
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type Windows
Name                         Type               Status
----                         ----               ------
SERVER01.CONTOSO.COM          Windows            Registered
SERVER02.CONTOSO.COM          Windows            Registered
```

Det första kommandot får valvet med namnet Vault03 med hjälp av cmdleten **Get-AzureRmBackupVault** .
Kommandot lagrar objektet i $Vault variabel.

Det andra kommandot får alla behållare av typen fönster från valvet i $Vault.

### Exempel 2: Hämta en specifik behållare
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type SCDPM -Name "DPMSERVER.CONTOSO.COM"
Name                         Type               Status
----                         ----               ------
DPMSERVER.CONTOSO.COM        SCDPM              Registered
```

Det här kommandot får behållaren DPMSERVER. CONTOSO.COM.
Kommandot anger valvet i $Vault och typen av container.

### Exempel 3: Visa alla registrerade virtuella Azure-datorer
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered 
Name                         Type               Status
----                         ----               ------
co03-vm                      AzureVM            Registered
```

Det här kommandot hämtar de registrerade virtuella datorerna från valvet i $Vault.

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

### -ManagedResourceGroupName
Anger namnet på den resurs grupp som är kopplad till behållaren.
Det här namnet är samma värde som du angav för parametern *ServiceName* eller *ResourceGroupName* för Register-AzureRmBackupContainer cmdleten.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namn
Anger namnet på den behållare som den här cmdleten får.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Anger aktuell status för de behållare som denna cmdlet får.
De acceptabla värdena för den här parametern är:

- NotRegistered 
- Rekommendera 
- Registreringen

```yaml
Type: AzureBackupContainerRegistrationStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Registered, Registering, NotRegistered

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Skriv
Anger den typ av behållare som den här cmdleten får.

```yaml
Type: AzureBackupContainerType
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, SCDPM, AzureVM, AzureBackupServer, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Valv
Anger ett säkerhets kopierings valv som den här cmdleten får behållare för.
För att få en **AzureRmBackupVault** , Använd cmdleten Get-AzureRmBackupVault.

```yaml
Type: AzureRMBackupVault
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

### AzureBackupVault

## VÄRDEN

### AzureBackupContainer

## ANMÄRKNINGAR
* Ingen

## RELATERADE LÄNKAR

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Register-AzureRmBackupContainer](./Register-AzureRmBackupContainer.md)

[Avregistrera-AzureRmBackupContainer](./Unregister-AzureRmBackupContainer.md)


