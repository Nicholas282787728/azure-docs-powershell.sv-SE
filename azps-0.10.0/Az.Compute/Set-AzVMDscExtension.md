---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDscExtension.md
ms.openlocfilehash: ccad3d793ec5763a4c7db44d2b5ff3583b35402b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924789"
---
# Set-AzVMDscExtension

## Sammanfattning
Konfigurerar DSC-tillägget på en virtuell dator.

## FRÅGESYNTAXEN

```
Set-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **set-AzVMDscExtension** konfigurerar tillägget DSC (önskad State Configuration) för Windows PowerShell på en virtuell dator i en resurs grupp.

## BESKRIVS

### Exempel 1: Ange ett DSC-tillägg
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

Det här kommandot anger DSC-tillägget på den virtuella datorn med namnet VM07 för att ladda ned Sample.ps1.zip från lagrings kontot med namnet STG och standard behållaren.
Kommandot anropar konfigurationen med namnet ConfigName.
Sample.ps1.zip filen har redan laddats upp med **publicering-AzVMDscConfiguration**.

### Exempel 2: Ange en DSC-anknytning med konfigurations data
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

Det här kommandot anger tillägget på den virtuella datorn med namnet VM13 för att ladda ned Sample.ps1.zip från lagrings kontot med namnet STG och behållaren med namnet WindowsPowerShellDSC.
Kommandot ConfigName och anger konfigurations data och argument.
Sample.ps1.zip filen har redan laddats upp med **publicering-AzVMDscConfiguration**.

### Exempel 3: Ange en DSC-anknytning med konfigurations data som har automatisk uppdatering
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

Det här kommandot anger tillägget på den virtuella datorn med namnet VM22 för att ladda ned Sample.ps1.zip från lagrings kontot med namnet STG och behållaren med namnet WindowsPowerShellDSC.
Kommandot anropar konfigurationen med namnet ConfigName och anger konfigurations data och argument.
Det här kommandot aktiverar också automatisk uppdatering av tilläggs hanteraren till den senaste versionen.
Sample.ps1.zip har tidigare laddats upp med **publicering-AzVMDscConfiguration**.

## MALLPARAMETRAR

### -ArchiveBlobName
Anger namnet på den konfigurations fil som tidigare laddades upp av Publish-AzVMDscConfiguration cmdleten.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConfigurationArchiveBlob

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ArchiveContainerName
Artens namn för Azure Storage-behållaren där konfigurations arkivet finns.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ArchiveResourceGroupName
Anger namnet på den resurs grupp som innehåller det lagrings konto som innehåller konfigurations arkivet.
Den här parametern är valfri om lagrings konto och virtuell dator finns i samma resurs grupp.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ArchiveStorageAccountName
Anger namnet på det Azure Storage-konto som används för att ladda ned ArchiveBlobName.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ArchiveStorageEndpointSuffix
Anger suffix för lagrings slut punkter.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoUpdate
Anger den versions hanterare som anges av parametern *version* .
Standard tilläggs hanteraren uppdateras inte automatiskt.
Använd parametern *AutoUpdate* för att aktivera automatisk uppdatering av tilläggs hanteraren till den senaste versionen som och när den är tillgänglig.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConfigurationArgument
Anger en hash-tabell som innehåller argumenten till funktionen konfiguration.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationData
Anger sökvägen till en. psd1-fil som anger data för konfigurationen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationName
Anger namnet på den konfiguration som DSC-tillägget anropar.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataCollection
Anger data insamlings typen.
De acceptabla värdena för den här parametern är: enable och Disable.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

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

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plats
Anger sökvägen till resurs tillägget.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namn
Anger namnet på Azure Resource Manager-resursen som representerar tillägget.
Standardvärdet är Microsoft. PowerShell. DSC.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Anger namnet på den virtuella datorns resurs grupp.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Anger vilken version av DSC-tillägget som Set-AzVMDscExtension använder inställningarna för.

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Anger namnet på den virtuella dator där DSC-tilläggsprovider är installerat.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WmfVersion
Anger WMF-versionen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 4.0, 5.0, 5.1, latest

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### Microsoft. Azure. commands. Compute. Models. PSAzureOperationResponse

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzVMDscExtension](./Get-AzVMDscExtension.md)

[Remove-AzVMDscExtension](./Remove-AzVMDscExtension.md)

[Publicera – AzVMDscConfiguration](./Publish-AzVMDscConfiguration.md)


