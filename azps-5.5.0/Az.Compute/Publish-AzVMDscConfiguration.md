---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/publish-azvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
ms.openlocfilehash: 94dac11a3c26adaac93b4e36c2dda3df513d4076
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211702"
---
# Publish-AzVMDscConfiguration

## SYNOPSIS
Laddar upp ett DSC-skript till Blob Storage i Azure.

## SYNTAX

### UploadArchive (standard)
```
Publish-AzVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateArchive
```
Publish-AzVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Publish-AzVMDscConfiguration** laddar upp ett DSC-skript (Desired State Configuration) till Azure blob-lagring, som senare kan användas på Azure-virtuella datorer med Set-AzVMDscExtension-cmdleten.

## EXEMPEL

### Exempel 1: Skapa ett ZIP-paket och ladda upp det till Azure-lagring
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1"
```

Det här kommandot skapar ett ZIP-paket för det givna skriptet och alla beroende resursmoduler och laddar upp det till Azure-lagring.

### Exempel 2: Skapa ett ZIP-paket och lagra det i en lokal fil
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

Det här kommandot skapar ett ZIP-paket för det givna skriptet och alla beroende resursmoduler och lagrar det i den lokala filen som heter .\MyConfiguration.ps1.zip.

### Exempel 3: Lägg till konfiguration i arkivet och ladda sedan upp det till lagring
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

Det här kommandot lägger till konfigurationen Sample.ps1 till konfigurationsarkivet för att ladda upp till Azure-lagring och hoppa över beroende resursmoduler.

### Exempel 4: Lägg till konfigurations- och konfigurationsdata i arkivet och ladda sedan upp det till lagring
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

Med det här kommandot läggs konfigurationsdata Sample.ps1 konfigurationsdata med namnet SampleData.psd1 till konfigurationsarkivet för överföring till Azure-lagring.

### Exempel 5: Lägga till konfiguration, konfigurationsdata och ytterligare innehåll i arkivet och ladda sedan upp det till lagring
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

Med det här kommandot läggs konfigurationen Sample.ps1, konfigurationsdata från SampleData.psd1 och ytterligare innehåll till konfigurationsarkivet för överföring till Azure-lagring.

## PARAMETERS

### -AdditionalPath
Anger sökvägen till en fil eller katalog som ska ingå i konfigurationsarkivet.
Den laddas ned till den virtuella datorn tillsammans med konfigurationen.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationDataPath
Anger sökvägen till en PSD1-fil som anger data för konfigurationen.
Det läggs till i konfigurationsarkivet och skickas sedan till konfigurationsfunktionen.
Den skrivs över av den konfigurationsdatasökväg som anges via Set-AzVMDscExtension-cmdleten

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationPath
Anger sökvägen till en fil som innehåller en eller flera konfigurationer.
Filen kan vara en Windows PowerShell-skriptfil (PS1) eller en fil med Windows PowerShell-modul (PSM1).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ContainerName
Anger namnet på azure-lagringsbehållaren som konfigurationen laddas upp till.

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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

### -Force
Tvingar kommandot att köras utan att användaren uppmanas att bekräfta.

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

### -OutputArchivePath
Anger sökvägen till en lokal ZIP-fil att skriva konfigurationsarkivet till.
När den här parametern används överförs konfigurationsskriptet inte till Blob Storage i Azure.

```yaml
Type: System.String
Parameter Sets: CreateArchive
Aliases: ConfigurationArchivePath

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den resursgrupp som innehåller lagringskontot.

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipDependencyDetection
Anger att den här cmdleten undantar DSC-resursberoenden från konfigurationsarkivet.

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

### -StorageAccountName
Anger azure-lagringskontots namn som används för att ladda upp konfigurationsskriptet till behållaren som anges av *containername-parametern.*

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEndpointSuffix
Anger suffixet för lagringsslutpunkten.

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bekräfta
Frågar dig om bekräftelse innan du kör cmdleten.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Visar vad som skulle hända om cmdleten körs.
Cmdleten körs inte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### System.String

### System.String[]

## UTDATA

### System.String

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzVMDscExtension](./Get-AzVMDscExtension.md)

[Remove-AzVMDscExtension](./Remove-AzVMDscExtension.md)

[Set-AzVMDscExtension](./Set-AzVMDscExtension.md)


