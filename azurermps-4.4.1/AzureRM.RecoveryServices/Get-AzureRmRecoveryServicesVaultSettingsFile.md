---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 56074606-28A6-4F91-A56C-4C8A9A31543F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesVaultSettingsFile.md
ms.openlocfilehash: 603cd65195f9e33c5006dcb4f2dc98ffc64aa7a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582235"
---
# Get-AzureRmRecoveryServicesVaultSettingsFile

## Sammanfattning
Hämtar inställningar för Azure Site Recovery-valvet.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### ForSite
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> -SiteIdentifier <String>
 -SiteFriendlyName <String> [[-Path] <String>] [-SiteRecovery] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByDefault
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-SiteRecovery]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ForBackupVaultType
```
Get-AzureRmRecoveryServicesVaultSettingsFile [-Vault] <ARSVault> [[-Path] <String>] [-Backup]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureRmRecoveryServicesVaultSettingsFile** hämtar inställnings filen för ett Azure Site Recovery-valv.

## BESKRIVS

### Exempel 1: registrera en Windows Server eller DPM-dator för Azure-säkerhetskopiering
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> $CredsPath = "C:\Downloads"
PS C:\> $Credsfilename = Get-AzureRmRecoveryServicesVaultSettingsFile -Backup -Vault $Vault01 -Path $CredsPath
```

Det första kommandot får valvet med namnet TestVault och lagrar det sedan i variabeln $Vault 01.

Det andra kommandot anger $CredsPath variabeln till C:\Downloads.

Det sista kommandot får valv filen för autentiseringsuppgifter för $Vault 01 genom att använda autentiseringsuppgifterna i $CredsPath för Azure Backup.

## MALLPARAMETRAR

### -Säkerhets kopiering
Anger att valvets autentiseringsinformation är tillämpbar för Azure Backup.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForBackupVaultType
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Anger sökvägen till inställnings filen för Azure Site Recovery-valvet.
Du kan ladda ned filen från portalen för Azure Site Recovery Vault och lagra den lokalt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteFriendlyName
Anger det eget namn för webbplatsen.
Använd den här parametern om du hämtar valv-autentiseringsuppgifterna för en Hyper-V-webbplats.

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteIdentifier
Anger webbplats-ID.
Använd den här parametern om du hämtar valv-autentiseringsuppgifterna för en Hyper-V-webbplats.

```yaml
Type: System.String
Parameter Sets: ForSite
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteRecovery
Anger att valv filen för valvet är tillämplig på Azure Site Recovery.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForSite, ByDefault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Valv
Anger Azure Site Recovery-valv objekt.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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

### ARSVault
Parametern ' valv ' godkänner värdet av typen ' ARSVault ' från pipeline

## VÄRDEN

### Microsoft. Azure. commands. RecoveryServices. VaultSettingsFilePath

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureRmRecoveryServicesVault](./Get-AzureRmRecoveryServicesVault.md)

[New-AzureRmRecoveryServicesVault](./New-AzureRmRecoveryServicesVault.md)

[Remove-AzureRmRecoveryServicesVault](./Remove-AzureRmRecoveryServicesVault.md)


