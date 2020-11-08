---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 51882269c342e766a3b714f931486eca437b9e58
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090857"
---
# Invoke-AzStorageSyncCompatibilityCheck

## Sammanfattning
Kontrollerar eventuella kompatibilitetsproblem mellan din dator och Azure-filsynkronisering.

## FRÅGESYNTAXEN

### PathBased (standard)
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### ComputerNameBased
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Invoke-AzStorageSyncCompatibilityCheck** kontrollerar eventuella kompatibilitetsproblem mellan din dator och Azure-filsynkronisering. Med en lokal eller fjärrsökväg utför den en uppsättning valideringar på systemet och fil namn rymden och returnerar sedan eventuella kompatibilitetsproblem som hittas.
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
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

Det här kommandot kontrollerar kompatibiliteten för systemet och även filer och mappar i C:\DATA.

### Exempel 2
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

Det här kommandot kontrollerar kompatibiliteten för filer och mappar i C:\DATA, men utför ingen kompatibilitetskontroll.

### Exempel 3
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen

## VÄRDEN

### Microsoft. Azure. commands. StorageSync. Evaluation. Models. PSValidationResult

## ANMÄRKNINGAR
* Nyckelord: Azure, AZ, arm, resurs, hantering, storagesync, FileSync

## RELATERADE LÄNKAR
