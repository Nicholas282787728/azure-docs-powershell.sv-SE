---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: AzureRM.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storagesync/invoke-azurermstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StorageSync/Commands.StorageSync/help/Invoke-AzureRmStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 73e0f00fe184a5462141b060717ca64567d4a67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578707"
---
# Invoke-AzureRmStorageSyncCompatibilityCheck

## Sammanfattning
Kontrollerar eventuella kompatibilitetsproblem mellan din dator och Azure-filsynkronisering.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### PathBased (standard)
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [-Quiet] [<CommonParameters>]
```

### ComputerNameBased
```
Invoke-AzureRmStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [-Quiet] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Invoke-AzureRmStorageSyncCompatibilityCheck** kontrollerar eventuella kompatibilitetsproblem mellan din dator och Azure-filsynkronisering. Med en lokal eller fjärrsökväg utför den en uppsättning valideringar på systemet och fil namn rymden och returnerar sedan eventuella kompatibilitetsproblem som hittas.
System kontroller:
- Fil namns namnrymd för webbläsarkompatibilitet kontrollerar:
- Tecken som inte stöds
- Maximal fil storlek
- Maximal Sök vägs längd
- Maximal fil längd
- Maximal mängd storlek
- Maximalt katalog djup

## BESKRIVS

### Exempel 1
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
```

Det här kommandot kontrollerar kompatibiliteten för systemet och även filer och mappar i C:\DATA.

### Exempel 2
```powershell
PS C:\> Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

Det här kommandot kontrollerar kompatibiliteten för filer och mappar i C:\DATA, men utför ingen kompatibilitetskontroll.

### Exempel 3
```powershell
PS C:\> $errors = Invoke-AzureRmStorageSyncCompatibilityCheck C:\DATA
PS C:\> $errors | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results
```

Det här kommandot kontrollerar kompatibiliteten för systemet och även filer och mappar i C:\DATA och exporterar sedan resultaten som en CSV-fil till C:\results.

## MALLPARAMETRAR

### -ComputerName
Den dator där du utför den här kontrollen.

```yaml
Type: System.String
Parameter Sets: ComputerNameBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Autentiseringsuppgift
Dina autentiseringsuppgifter för den delning du verifierar.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
UNC-sökvägen för den resurs som du verifierar.

```yaml
Type: System.String
Parameter Sets: PathBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Quiet
Utelämnar Skriv ut rapport till konsol.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipNamespaceChecks
Ange den här flaggan för att hoppa över valideringar av fil namn områden och endast utföra system verifieringar.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PathBased
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipSystemChecks
Ange den här flaggan för att hoppa över system verifieringar och endast utföra verifieringar av fil namn.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen

## VÄRDEN

### Microsoft. Azure. commands. StorageSync. Evaluation. Models. PSValidationResult

## ANMÄRKNINGAR
* Nyckelord: Azure, azurerm, arm, resurs, hantering, storagesync, FileSync

## RELATERADE LÄNKAR
