---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 51882269c342e766a3b714f931486eca437b9e58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231519"
---
# Invoke-AzStorageSyncCompatibilityCheck

## SYNOPSIS
Söker efter potentiella kompatibilitetsproblem mellan systemet och Azure File Sync.

## SYNTAX

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

## BESKRIVNING
Cmdleten **Invoke-AzStorageSyncCompatibilityCheck** söker efter potentiella kompatibilitetsproblem mellan systemet och Azure File Sync. Givet en lokal sökväg eller fjärrsökväg utför den en uppsättning verifieringar på systemet och i filnamnsområdet och returnerar sedan eventuella kompatibilitetsproblem som hittas.
Systemkontroller:
- OS-kompatibilitet Filnamnsrymden kontrollerar:
- Tecken som inte stöds
- Maximal filstorlek
- Maximal sökvägslängd
- Maximal fillängd
- Maximal datauppsättningsstorlek
- Maximalt katalog djup

## EXEMPEL

### Exempel 1
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

Det här kommandot kontrollerar kompatibiliteten för systemet samt filer och mappar i C:\DATA.

### Exempel 2
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

Det här kommandot kontrollerar kompatibiliteten för filer och mappar i C:\DATA, men utför ingen systemkompatibilitetskontroll.

### Exempel 3
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

Det här kommandot kontrollerar kompatibiliteten för systemet samt filer och mappar i C:\DATA och exporterar sedan resultaten som en CSV-fil till C:\resultat.

## PARAMETERS

### -Datornamn
Den dator som du utför den här kontrollen på.

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

### -Credential
Dina autentiseringsuppgifter för den delning som du validerar.

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
UNC-sökvägen för den delning som du validerar.

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
Ställ in den här flaggan om du vill hoppa över namnområdesverifieringar och endast utföra systemverifieringar.

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
Ställ in den här flaggan om du vill hoppa över systemverifieringar och bara utföra namnområdesverifieringar.

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
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### Ingen

## UTDATA

### Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult

## ANTECKNINGAR
* Nyckelord: azure, Az, arm, resource, management, storagesync, filesync

## RELATERADE LÄNKAR
