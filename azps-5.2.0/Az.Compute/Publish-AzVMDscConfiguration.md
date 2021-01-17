---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/publish-azvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
ms.openlocfilehash: 94dac11a3c26adaac93b4e36c2dda3df513d4076
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391208"
---
# Publish-AzVMDscConfiguration

## Sammanfattning
Laddar upp ett DSC-skript till Azure Blob Storage.

## FRÅGESYNTAXEN

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

## PROBLEMBESKRIVNING
Cmdleten **Publishing-AzVMDscConfiguration** laddar upp ett DSC-skript (Desired State Configuration) till Azure Blob Storage, som senare kan tillämpas på virtuella Azure-datorer med cmdleten Set-AzVMDscExtension.

## BESKRIVS

### Exempel 1: skapa ett zip-paket ett Ladda upp i Azure Storage
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1"
```

Det här kommandot skapar ett. zip-paket för det angivna skriptet och eventuella underordnade moduler och uppladdar det till Azure Storage.

### Exempel 2: skapa ett zip-paket och lagra det i en lokal fil
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

Det här kommandot skapar ett. zip-paket för det angivna skriptet och eventuella underordnade moduler och lagrar dem i den lokala filen som heter .\MyConfiguration.ps1.zip.

### Exempel 3: lägga till konfigurationen i arkivet och sedan överföra den till lagrings plats
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

Det här kommandot lägger till konfigurationen som heter Sample.ps1 i konfigurations arkivet för överföring till Azure-lagring och hoppar över moduler som är underordnade.

### Exempel 4: lägga till konfigurations-och konfigurations data i arkivet och sedan överföra det till lagrings utrymme
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

Det här kommandot lägger till konfigurationen som heter Sample.ps1 och konfigurations data med namnet SampleData.psd1 i konfigurations arkivet för överföring till Azure Storage.

### Exempel 5: lägga till konfiguration, konfigurations data och ytterligare innehåll i arkivet och sedan överföra det till lagrings utrymme
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

Det här kommandot lägger till konfigurationen med namnet Sample.ps1, konfigurations data SampleData.psd1 och ytterligare innehåll i konfigurations arkivet för överföring till Azure Storage.

## MALLPARAMETRAR

### -AdditionalPath
Anger sökvägen till en fil eller en katalog som ska ingå i konfigurations arkivet.
Den laddas ner till den virtuella datorn tillsammans med konfigurationen.

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
Anger sökvägen till en. psd1-fil som anger data för konfigurationen.
Detta läggs till i konfigurations arkivet och överförs sedan till funktionen konfiguration.
Den skrivs över av konfigurations data Sök vägen via Set-AzVMDscExtension cmdlet

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
Filen kan vara en Windows PowerShell-skriptfil (. ps1) eller en Windows PowerShell-modul (. psm1).

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
Anger namnet på den Azure Storage-behållare som konfigurationen laddas upp till.

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
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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
Tvingar kommandot att köras utan att fråga efter bekräftelse.

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
Anger sökvägen till en lokal zip-fil för att skriva konfigurations arkivet till.
När den här parametern används laddas inte konfigurations skriptet till Azure Blob Storage.

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
Anger namnet på den resurs grupp som innehåller lagrings kontot.

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
Anger att denna cmdlet exkluderar DSC-resurstilldelningar från konfigurations arkivet.

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
Anger namnet på det Azure Storage-konto som används för att ladda upp konfigurations skriptet till den behållare som anges av *ContainerName* -parametern.

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
Anger suffixet för lagrings slut punkten.

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
Du uppmanas att bekräfta innan du kör cmdleten.

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
Visar vad som händer om cmdleten körs.
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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### System. String

### System. string []

## VÄRDEN

### System. String

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzVMDscExtension](./Get-AzVMDscExtension.md)

[Remove-AzVMDscExtension](./Remove-AzVMDscExtension.md)

[Set-AzVMDscExtension](./Set-AzVMDscExtension.md)


